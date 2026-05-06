
# a11g-final-submission

**Team Number: 06**

**Team Name: 404 Firmware Not Found**

| Team Member Name  | Email Address          | GitHub Username |
| ----------------- | ---------------------- | --------------- |
| Praise Ndlovu     | praisen@seas.upenn.edu | pbn107          |
| Anjali Jathavedam | apjath@seas.upenn.edu  | apjath          |

## 1. Video Presentation

Link: https://youtu.be/fIFFB9PDKGI 

## 2. Project Summary

The DSPiano is a compact, multi-functional piano that allows users to play notes in a four octave range,
 display the waveform of each note, and record their tune if desired. Users are able to play in free-play mode, 
 or learn how to play sheet music in note-play mode.

As avid music-enjoyers, we were inspired to build a product that is easy to use and 
allows for experimentation with music. We have both wanted to learn the piano and thought creating
a device that facilitates the learning process would be a great opportunity.

We additionally appreciate that the device is simple enough to use for a very wide range of ages,
yet has functionality that will keep it interesting despite age of the user.

We used Internet connection to allow users to play music through their computer for added portability
of the product. Using the Internet also allowed us to create a robust user interface that can be easily 
navigated and add recording functionality. 

Device Functionality

The user-interface of our device includes the Node-Red dashboard, an LCD screen mounted to the product,
and the 8 keys that function as one octave of a piano. Under this layer of abstraction,
we created a custom PCBA that can be powered via LiPo or USB connection 

Explain how your Internet-connected device is designed
Include sensors, actuators, and other critical components.
Include your system-level block diagram here.

Challenges

We faced a few significant challenges throughout the semester. After submitting our PCB files for manufacturing,
we were made aware that our I2C footprint could not be matched to any existing I2C expander. We did not consider this 
possibility during the creation of the board, so did not budget any pins on the chip for general back-up GPIO use. 
We initially solved this by buying off-board I2C expanders. 

Another challenge we faced was the small error of grounding SWO in our schematic, making it impossible to flash
to our PCBA. We examined our schematic to find the issue and were able to cut traces on the PCBAs in order to 
flash to them. 

The most significant challenges we faced were with the codebase. We were able to run I2C and SPI separately, but 
when we attempted to run them together in the integrated codebase, one would fail. We iterated on this problem
for over a week, using several different programs for I2C and SPI, but unfortunately we simply could not get both to work at once.
We decided to prioritize SPI for our
LCD screen and decided to use a development board for GPIO pins to connect our buttons. 

The last challenge we faced was with over the air firmware updates (OTAFU). Despite being able to remotely flash to our board
in the A08 assignment, we faced difficulty hosting both mqttIn and mqttOut in one WiFi instance. When we kept each process separate,
we were able to use our intended Internet functionality and OTAFU.

Where did you face difficulties? This could be in firmware, hardware, software, integration, etc.
How did you overcome these challenges?

Prototype Learnings



What lessons did you learn by building and testing this prototype?
What would you do differently if you had to build this device again?
Next Steps & Takeaways
What steps are needed to finish or improve this project?
What did you learn in ESE5160 through the lectures, assignments, and this course-long prototyping project?
Project Links
Provide a URL to your Node-RED instance for our review (make sure it’s running on your Azure instance!)
Provide the share link to your final PCBA on Altium 365.
Consider downloading your PCBA source and manufacturing files to keep after you leave UPenn. Your Altium access will expire after this semester.


## 3. Hardware & Software Requirements

## 4. Project Photos & Screenshots

![1777933352674](image/README/1777933352674.png)

![1777933369984](image/README/1777933369984.png)

![1777933293641](image/README/1777933293641.png)

![1777933316114](image/README/1777933316114.png)

![1777933513532](image/README/1777933513532.jpg)

![1777933533687](image/README/1777933533687.png)

![1777933848196](image/README/1777933848196.png)

![1777933856384](image/README/1777933856384.png)

![1777933716868](image/README/1777933716868.png)

![1777933686708](image/README/1777933686708.png)

## 5. Codebase

Do *not* commit any of your source code to this repository. Rather, provide links to the other GitHub repository you've already been using with your firmware.

- A link to your final embedded C firmware codebases
- A link to your Node-RED dashboard code
- Links to any other software required for the functionality of your device
