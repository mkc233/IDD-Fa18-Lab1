# IDD-Fa19-Lab1: Blink!

**A lab report by Michael Chan**


## Part A. Set Up a Breadboard

[insert a photo of your breadboard setup here]


## Part B. Manually Blink a LED

**a. What color stripes are on a 220 Ohm resistor?**
A 220 Ohm resistor has 5 stripes, 2 red, 2 black and then 1 brown.  The first three stripes indicate that its 220 ohms, the 4th stripe is black and indicates that the multiplier factor is 1.  The final strip is brown and indicates the tolerance of +/- 1%.  
 
**b. What do you have to do to light your LED?**
To light the LED the button must be depressed.  When the button is pushed the circuit becomes closed and allows for current to pass through the LED and light it.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

[Original Blinking Code](https://github.com/mkc233/IDD-Fa18-Lab1/blob/master/originalBlinkCode)

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**
The digitalWrite(LED_BUILTIN, HIGH) determines when the LED turns on, while the digitalWrite(LED_BUILTIN, LOW) determines when the LED turns off.  To make the LED blink its necessary to put a delay so that it turns on, waits and then turns off to simulate blinking.
**b. What line(s) of code do you need to change to change the rate of blinking?**
To change the rate of blinking the delay(1000) needs to be changed in order to make it faster or slower.  A smaller number will lead to faster blinking and vice versa.
**c. What circuit element would you want to add to protect the board and external LED?**

 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**
At a delay of 10 ms I can no longer perceive the LED as blinking.  

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[link to your video here; feel free to upload to youtube and just paste in a link here]


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**


## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

**b. What is analogWrite()? How is that different than digitalWrite()?**


## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

**d. Is information stored in your device? Where? How?**

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
