![alt text][logo]
[logo]: https://avatars0.githubusercontent.com/u/7002937?v=3&s=200 "Logo Title Text 1"

## Pulse Sensor Arduino Code
1. Blinks an LED to User's Live Heartbeat   
2. Fades an LED to User's Live HeartBeat
3. Determines BPM
4. Prints All of the Above to Serial

## Screen Shot
![alt text][screenshot]
[screenshot]: https://github.com/WorldFamousElectronics/PulseSensor_Amped_Arduino/blob/master/pics/ScreenCapArduino.png "Screen Shot" 


## To Use:
1. Take the entire file 'PulseSensorAmped_Arduino_1dot1' into your Documents/Arduino.
2. Then start, or restart Arduino IDE and find the code in your Sketch folder.


## Pulse Sensor Hook-up
Arduino Pin   | Pulse Sensor Cable Color
------------- | -------------
RED           | 5V or 3V   
BLACK         | GND (GROUND)
PURPLE        | ANALOG 0 (Zero)

##Variables to Note
Variable Name     | What it does
------------------| -------------
Signal            | **Int** that holds **raw Analog Input data on **Pin 0**, the Pulse Sensor's **Purple Cable**. It's updated every 2mS.
BPM               | **Int** that holds the **heart-rate value**, derived every beat, from averaging **previous 10 IBI values**. 
IBI               | **Int** that holds the **time interval between beats**! Must be seeded! 
Pulse             | **Boolean** that is **true when a heartbeat is sensed**. It's **false** other times.  It **controls LED Pin 13**.
QS                | **Boolean** that is **true whenever Pulse is found and BPM** is updated. User must reset. 



## Serial Output
This code is designed with output serial data.
The serial Data can be used/viewed:
* In the Arduino Serial Monitor  `Arduino >> Tools >> Serial Monitor`
* With our <a href="https://github.com/WorldFamousElectronics/PulseSensor_Amped_Processing_Visualizer"> "Processing Visualizer"</a>
* In our native Mac App (TBA Spring 2015) 
* Any any third-party serial reader.



## (Advanced) Timer Interrupt Notes / PWM on Pin 3 & 11
There is a tab in the Arduino code called Timer_Interrupt_Notes. This page describes how to set up the Timer interrupt depending on which version of Arduino you are using, and what other things you may want to do with your sketch. Please read it carefully!

PWM on pins 3 and 11 will not work when using this code, because we are using Timer 2!


## The Video
<a href="https://vimeo.com/123008578"> "The Pulse Sensor in 60 Seconds"</a>
