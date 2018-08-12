# Aurdino-Knock-Lock
This Aurdino based secret knocking system reads vibrations and responds accordingly(i.e. opens if number of vibrations matches set value).
A piezo buzzer usually creates vibrations, but here i have used it as an input to detect how many times someone knocks on your door.When the piezo is pressed flat against a solid surface that can vibrate (like a wooden table top) our Arduino can sense the vibrations and read them with the analog input pins. Using this information the Arduino program can count how many times someone has knocked .Then using a servo motor, it automatically opens the door if someone knocks the right number of times!
In this project, I have set a certain number of knocks as a secret code for opening a box. If someone knocks the right number of times, the box unlocks by moving the arm of a servo motor!

 The following electrical components is required for this project:

1 pushbutton

1 piezo component

3 LEDs (red, yellow, and green)

3 220 ohm resistors

1 10 k-ohm resistor

1 M-ohm resistor

1 100 uF capactior

1 servo motor ...and of course your Arduino Uno and a breadboard!
