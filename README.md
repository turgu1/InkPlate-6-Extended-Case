# InkPlate-6-Extended-Case

This is a change to the current InkPlate-6 case to add a small electronic board with push buttons below the mainboard. To do it, I took the original design from e-Radionica and extended a side of it, so the original portion of the case remains unchanged. The Mechanical folder contains the complete STEP format design as well as the STL ready for 3D printing. The Electronics folder contains the Gerber files for the preparation of the pc-board, as well as the schematic in PDF. 

- For the STL, dimensions are in millimeters. 
- Six buttons must be printed as well as the top and bottom casing.
- The connection with the MCU23017 is done using wirewrap wires that are soldered using the following configuration (beware that some numbers are inverted):

```
On the Buttons PCB  | On the InkPlate Board
--------------------+----------------------
                    |
     Pin 1          |       GND           
     Pin 2          |       GPB2           
     Pin 3          |       GPB4
     Pin 4          |       GPB3
     Pin 5          |       GPB5
     Pin 6          |       GPB7
     Pin 7          |       GPB6
```

- The three tactical pads must be disabled, the corresponding signals from the MCU23017 are diverted to the GPBx pin holes on the pc-board. This is done by desoldering the current jumpers and soldering them back on the other side. They are located under the following labeling on the board: "Touch pads".

- The corresponding GPIOB I/O bits corresponding to the GPB2-7 pins of the MCU23017 must have their internal pull-up resistor enabled.

- The buttons' pc-board must be of a standard height (1.6 mm). This to ensure proper spacing for the buttons. The board must be 'glued' at the bottom of the main casing using two-sided scotch tape. An alternative would be using a very small amount of hot glue on the 4 corners on the top of the buttons' pc-board. This is to permit easy removal in case of problems.

The original licensing from e-Radionica remains GPL-3 for their design and all supplied files in this project.

<img src="Pictures/Inkplate_6_With_Mechanical_Buttons.png" alt="picture" width="600"/>
<img src="Pictures/Bottom_Case_With_Buttons_Board.png" alt="picture" width="300"/><img src="Pictures/Buttons 3D View.png" alt="picture" width="300"/>
