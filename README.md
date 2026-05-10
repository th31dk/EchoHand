<h1 align="center">
    EchoHand
</h1>
<h4 align="center">
    A robot hand that mirror's your every gesture
</h4>

![image](/assets/zine_v2.png)

<h2 align="center">
A Bit About This Project
</h2>
This project originally started as a ASL Interpreter. However, while researching ways to teach it signs, I discovered computer vision and how you can make robots copy you. Last year, I went to Prototype, a hackathon hosted by Hack Club. There, we had to train these SO-101 Robotic Arms to perform certain actions. The teleoperator part of the training stuck to me the most, so this project was born!

<h2 align="center">
Assembly
</h2>

![image](/assets/fullarm_v2_4.png)

### Hardware
#### [Bill Of Materials](/BOM)
|Part Number|Part Name            |Quantity|Sourcing Link                                       |Cost  |Notes|
|-----------|---------------------|--------|----------------------------------------------------|------|-----|
|1          |Arduino Uno          |1       |https://www.aliexpress.us/item/3256808569187520.html|$5.65 |     |
|2          |Breadboard           |1       |https://www.aliexpress.us/item/3256806927240551.html|$1.92 |     |
|3          |Dupont Wires         |17      |https://a.co/d/0hN85zCM                             |$8.99 |     |
|4          |External Power Supply|1       |https://a.co/d/045DWk0g                             |$59.99|     |
|5          |DS3225 Servo         |5       |https://a.co/d/0iK4KOZB                             |$90.00|     |
|6          |M3x10mm BHCS         |24      |https://www.aliexpress.us/item/2255800794906149.html|$1.86 |     |
|7          |M3x10mm SHCS         |2       |https://www.aliexpress.us/item/3256804341271555.html|$1.50 |     |
|8          |USB-A to USB-B Cable |1       |https://a.co/d/0aNsTbvj                             |$7.21 |     |
|9          |Webcam               |1       |https://a.co/d/0bebSZXz                             |$25.00|     |
|10         |Fishing Line         |2000mm  |https://a.co/d/07G4QxGr                             |$9.98 |     |
|11         |Elastic Cord         |600mm   |https://a.co/d/07XXOlZX                             |$9.99 |     |

### [3D Printed Parts](/List%20Of%203D%20Printed%20Parts.csv)
3D files can be found [here](/Print%20Files/)

|Part Number|Part Name            |Quantity|Material                                            |Total Grams|Notes                        |
|-----------|---------------------|--------|----------------------------------------------------|-----------|-----------------------------|
|1          |Finger 1             |5       |PLA                                                 |17.69      |                             |
|           |                     |        |PETG                                                |0.34       |PETG for easy support removal|
|2          |Finger 2             |5       |PLA                                                 |20.15      |                             |
|           |                     |        |PETG                                                |0.38       |PETG for easy support removal|
|3          |Finger 3             |4       |PLA                                                 |14.95      |                             |
|           |                     |        |PETG                                                |0.37       |PETG for easy support removal|
|4          |Thumb                |1       |PLA                                                 |7.33       |                             |
|           |                     |        |PETG                                                |0.77       |PETG for easy support removal|
|5          |BackStand            |1       |PLA                                                 |133.6      |                             |
|6          |Palm                 |1       |PLA                                                 |28.9       |                             |
|7          |Pin                  |11      |PLA                                                 |0.71       |                             |
|8          |Spool                |10      |PLA                                                 |23.44      |                             |
|9          |Support              |1       |PLA                                                 |44.39      |                             |

### Wiring Diagram
![image](/assets/finalSchematic.png)

### Assembly Instructions
1. Put together all of the fingers. Align each of the segments together and use the pin to keep them together
2. Secure all of the fingers to the palm using a 70mm piece of PLA
3. Screw the palm onto the back plate with 2 M3x10BHCS
4. Screw in all the servos to the servo mounts with 10 M3x10 BHCS. The servo orientation should match the orientation in the assembly model.
5. Screw the servo mount into the back plate with 2 M3x10 BHCS
6. Screw the support bracket onto the back plate with 2 M3x10 BHCS and 2 M3x10 SHCS
7. Assemble the spools with 10 M3x10 BHCS. Only screw in the middle screw enough to keep it from spinning. 
8. Tie down each of the fingers to the palm using the elastic cord. Only tie it to the point where it can return to the original position after being pulled down
9. Thread the fishing line through each of the holes under the palm through the fingers and tie it so that it doesn't become loose when pulled. Make sure to leave at least 220mm of fishing line hanging from the bottom 
10. Connect all the wires according to the [wiring diagram](/assets/finalSchematic.png)
11. Download the [Arduino IDE](https://www.arduino.cc/en/software/)
11. Connect the Arduino Uno to your computer and upload [main.ino](/code/main.ino) to it.
12. Open the serial monitor on the Arduino IDE and set it to 9600 baud. You should see "Ready!"
13. Set all of the servos to 0. In the serial monitor, type the first letter of the finger name followed by 0. 
14. Place the horns facing 180 degrees away from the holes on the bottom of the palm.
15. Line up the screws on the spool with the horns and tighten the middle screw so it is firmly attached to the servo. 
16. Lead each fishing line it the way that the servo spins. Then, loop it twice through the spool hole and tie it off. Make sure that it's very tight. 
17. Adjust the angle of each of the servos until it goes down fully. Then note down that angle.
18. Download [main.py](/code/main.py)
19. Adjust each of the finger angles according to what you wrote down
20. Run the code!

[Here's the Demo!](https://www.youtube.com/watch?v=Rfja3hf1nRA)

### Credits
Thank you to:  
Hack Club for supporting me throughout this project

Made by Horizon on Youtube for inspiring me to make this project. Check his [robotic hand](https://www.youtube.com/watch?v=aHFo-7ZK1Bk&t=697s) out!

MateoTechLab for making the amazing videos that encouraged me to make this and pursue hardware! Go watch his video [here](https://www.youtube.com/watch?v=NimROnJeQDY&t=253s)!

notaroomba for his amazing README layout! His [Trace](https://github.com/notaroomba/trace) project is super cool!