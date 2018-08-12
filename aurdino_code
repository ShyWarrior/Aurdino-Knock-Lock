#include<Servo.h>
Servo myServo;
const int piezo=A0;
const int switchPin=2;
const int yellowLed=3;
const int greenLed=4;
const int redLed=5;
int knockVal;
int switchVal;
const int quietKnock=10;
const int loudKnock=100;
boolean locked=false;
int numberofknocks=0;









void setup(){
 
  
	myServo.attach(9);
    pinMode(yellowLed,OUTPUT);
	pinMode(redLed,OUTPUT);
	pinMode(greenLed,OUTPUT);
	pinMode(switchPin,INPUT);
	Serial.begin(9600);
	digitalWrite(greenLed,HIGH);
	myServo.write(0);
  	Serial.println("The box is unlocked!");


}
    
void loop(){
  

     if(locked==false){
    switchVal=digitalRead(switchPin);
    if(switchVal==HIGH)
    {
      locked=true;
     digitalWrite(greenLed,LOW);
     digitalWrite(redLed,HIGH);
     myServo.write(90);
     Serial.println("The box is locked");
     delay(1000);
    }
  }
    if(locked==true){
      knockVal=analogRead(piezo);
      if(numberofknocks<3&&knockVal>0){
        if(checkForKnocks(knockVal)==true){
          numberofknocks++;
        }
        Serial.print(3-numberofknocks);
        Serial.print("more knocks to go");}
        if(numberofknocks>=3){
          locked=false;
          myServo.write(0);
          delay(20);
          digitalWrite(greenLed,HIGH);
          digitalWrite(redLed,LOW);
          Serial.println("The box is unlocked!");
  

      }
    }    


}
boolean checkForKnocks(int value){
  if(value>quietKnock&&value<loudKnock){
   digitalWrite(yellowLed,HIGH);
    delay(50);
    digitalWrite(yellowLed,LOW);
    Serial.print("Valid knock of value");
    Serial.println(value);
    return true;
  }
  else{
    Serial.print("Bad knock value");
    Serial.println(value);
    return false;
  }
}
  
