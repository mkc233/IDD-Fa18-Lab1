# IDD-Fa19-Lab1: Blink!

**A lab report by Michael Chan**


## Part A. Set Up a Breadboard

![Breadboard Setup](https://github.com/mkc233/IDD-Fa19-Lab1/blob/master/Breadboard_Setup.jpg)


## Part B. Manually Blink a LED

**a. What color stripes are on a 220 Ohm resistor?**
A 220 Ohm resistor has 5 stripes, 2 red, 2 black and then 1 brown.  The first three stripes indicate that its 220 ohms, the 4th stripe is black and indicates that the multiplier factor is 1.  The final strip is brown and indicates the tolerance of +/- 1%.  
 
**b. What do you have to do to light your LED?**
To light the LED the button must be depressed.  When the button is pushed the circuit becomes closed and allows for current to pass through the LED and light it.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

[Original Blinking Code](https://github.com/mkc233/IDD-Fa19-Lab1/blob/master/code/originalBlinkCode)

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**
The digitalWrite(LED_BUILTIN, HIGH) determines when the LED turns on, while the digitalWrite(LED_BUILTIN, LOW) determines when the LED turns off.  To make the LED blink its necessary to put a delay so that it turns on, waits and then turns off to simulate blinking.

**b. What line(s) of code do you need to change to change the rate of blinking?**
To change the rate of blinking the delay(1000) needs to be changed in order to make it faster or slower.  A smaller number will lead to faster blinking and vice versa.

**c. What circuit element would you want to add to protect the board and external LED?**
I would want to add a surge protector to protect both the board and external LED from voltage spikes.
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**
At a delay of 10 ms I can no longer perceive the LED as blinking.  Using the the camera from my phone I can now see that the LED is indeed still blinking.  In addition, per the code there is both a High and low digitalWrite() line indicating the LED is being turned on and off.

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**

[My Blink](https://github.com/mkc233/IDD-Fa19-Lab1/blob/master/code/myBlink)


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[LED Blinking](https://www.youtube.com/watch?v=IVfwgCXlV_M)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**
Yes i was able to get the LED to glow the whole turning range.  Even at the minimum current, there was enough to light up the LED.


## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
The pinmode in the setup has be changed to number 11 in order to control the circuit using pin 11.  It has to be changed in the void loop() as well to pin 11 when analgWrite() is used. 

**b. What is analogWrite()? How is that different than digitalWrite()?**
analogWrite() is used for pin11 because it has PWM control allowing for a range of voltages being applied to the pin.  Digitalwrite() is only capable of sending all the voltage or none of the voltage.

## Part F. FRANKENLIGHT!!!

![Remote Control PCB 1]()
![Remote Control PCB 2]()
[Schematic]

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**
There are a number of microprocessors within the remote control PCB.  There are 2 small ones towards the LED, and 1 larger one and smaller one in the middle.  The microprocessor is most likely determining which infared code to send to the TV when certain buttons are pressed.  

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**
There don't seem to be any sensors on the remote.  There are numerous pressure activated points in the circuit which seem to respond to presses on the remote. There is an infared light on the remote which sends signals to the TV.

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**
The device is powered using two AA batteries at 1.5 volts, for a total of 3 volts.  It appears to be run at 3 volts throughout the remote.  There does not appear to be any voltage transmission or regulation.  

**d. Is information stored in your device? Where? How?**
The microprocessor most likely stores the infared codes when the corresponding button on the remote is pressed.  There are a number of microprocessors located on the PCB.

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

Given that the batteries are providing 3 volts, any point on the PCB should be able to provide enough voltage to power the LED.  I connected the LED across one of the capacitors and it lit up.  

### 3. Build your light!

[Frankenlight Video](https://youtu.be/nDJ_xCq2KSs)
