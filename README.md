# SmartFactory_I2cCommunication

The i2c interface is a serial data bus to connect low speed devices. The data is transmitted via two cables, one being the clock line and the other being the data line. The i2c interface is based on the master-slave principle, whereby the master can push and pull messages to the slave. It is also possible to have more than one master in a system. The slave is identified by its address, with a microcontroller as slave the address can be freely selected, as long as no other slave has the address. 
In the SmartFactory project, data is exchanged between the SorticRobot and the SorticRobot CommunicationHub via the i2c interface. In the principle of a template, predefined structs are sent and received byte by byte. This enables a simple data exchange between the two closely linked systems. The i2c interface can also be used to read sensors if desired.

## Table of contents

- Tools and technologies
   - Visual Studi Code
   - Doxygen
   - I2C
- Hardware
   - Logic Level converter
- Software
   - I2C
   - UML
   - Dependency Graph
   - Collaboration Diagram
- ToDo's

## Tools and technologies

The source code is implemented in the programming language C++. In the following, the tools for editing the project are listed.

#### Visual Studio Code

The development environment used is [Visual Studio Code](https://code.visualstudio.com/) with the [PlatformIO extension](https://docs.platformio.org/en/latest/ide/vscode.html). The development environment can be downloaded for free. For an installation guide look here.  

#### Doxygen

Doxygen was used for documentation of the source code. For using Doxygen in Visual Studio code, the [Doxygen Documentation Generator](https://marketplace.visualstudio.com/items?itemName=cschlosser.doxdocgen) extension can be used.

#### I2C

The binary signals for the i2c communication are generated by pull-up resistors. The clock line gives a time-delayed periodic square wave signal, which defines the clock of the transmission. The data bits are transmitted by a time-delayed aperiodic square-wave signal on the data line. For a more detailed explanation [here](http://www.circuitbasics.com/basics-of-the-i2c-communication-protocol/).

![i2c](http://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-I2C-Data-Transmission-Diagram-ADDRESS-FRAME-2.png)
[Image: [Circuit Base: I2C COMMUNICATION PROTOCOLL](http://www.circuitbasics.com/basics-of-the-i2c-communication-protocol/)]

## Hardware

#### Logic Level converter

A logic level converter is used to convert the different voltages of the binary signals. An explanation of the Logic Level converter can be found [here](https://www.instructables.com/id/A-Quick-Guide-on-Logic-Level-Shifting/).

![converter](https://cdn-shop.adafruit.com/1200x900/757-03.jpg)
[Image: [Adafruit: LOGIC LEVEL CONVERTER](https://www.adafruit.com/product/757)

## Software

#### I2C

The i2c interface was implemented by preprocessor instructions for the connection as master or slave in the same interface. By uncommenting "#define MASTER" the slave version can be used.
```
// UNCOMMIT IF SLAVE

#define MASTER 
```

#### UML

The figure below shows the data model in UML notation. 

================== IMAGE ===============================

#### Dependency Graph

The figure below shows the dependency tree of the I2cCommunication interface.


 ==================== IMAGE ==================================
 
 
 
#### Collaboration Diagram

The figure below shows the collaboration tree of the I2cCommunication interface. The arrow simbolizes an instanced object.

=================== IMAGE ==========================================

## ToDo's
- [ ]
- [ ]
