# Problem-diagram
D. Jin, C. Wang and Z. Jin, "Automating Extraction of Problem Diagrams from Natural Language Requirement Documents," 2023 IEEE 31st International Requirements Engineering Conference Workshops (REW), Hannover, Germany, 2023, pp. 199-204, doi: 10.1109/REW57809.2023.00039.

下图为上述参考文献中通过设计神经网络模型从需求文档中提取建模元素，然后将它们组装成问题图。

该文献中使用sun search control system生成的问题图经过专家的讨论和评价，得出以下结论:

1.问题图中的A serial Port应该是外部设备的属性，所以不应该作为实体，其他节点都是正确的，所以正确性是15/16。

2. SS和DMC之间的共享现象没有被识别到，其他识别的现象都是正确的。

![Problem-diagram](https://user-images.githubusercontent.com/98217021/230363993-bd3ffacc-3f73-4f8b-84c1-98768e06dcab.png)


以下是通过使用我们设计的提示词从sun search control system需求文本中提取到的建模元素

可以看到在Phenomenon Sharing中我们可以成功提取到SS和DMC之间的共享现象（加粗部分）

#Machine Domain
- Sun Search Control Software

#Given Domain
- Gyroscopes
- Sun Sensors
- Three-axis Control Thrusters
- Data Management Computer
- Control Computer CPU
- Satellite
- Mode Register
- Timer
- Analog-to-Digital Converter
- Digital Tube
#Design Domain
- Serial Ports
- Timing Control Register

#Requirement Domain
- <Satellite, Reference, Attitude Determination>
- <Gyroscopes, Reference, Data Acquisition>
- <Sun Sensors, Reference, Data Acquisition>
- <Three-axis Control Thrusters, Reference, Control>
- <Data Management Computer, Reference, Command Processing>
- <Gyroscopes, Constraint, Data Acquisition Command>
- <Gyroscopes, Constraint, Measurement Data>
- <Sun Sensors, Constraint, Angle Measurement Data>
- <Sun Sensors, Constraint, Sun Visible Flag>
- <Three-axis Control Thrusters, Constraint, Power Status Signal>
- <Three-axis Control Thrusters, Constraint, Thruster Control>
- <Sun Sensors, Reference, Sun Sensor Switching Instruction>
- < Analog-to-Digital Converter, Constraint, Data Conversion>
- < Analog-to-Digital Converter, Reference, Signal Collection>
- < Digital Tube, Reference, Telemetry Data Transmission >

#Phenomenon Sharing
- <Sun Sensors, Sun Search Control Software, Sun Measurement Angle>
- <Sun Sensors, Sun Search Control Software, Sun Visible Flag>
- <Gyroscopes, Sun Search Control Software, Angular Velocity Measurement Data>
- <Gyroscopes, Sun Search Control Software, Angular Velocity Analog Signal>
- <Three-axis Control Thrusters, Sun Search Control Software, Three-axis Torque Control>
- <Data Management Computer, Sun Search Control Software, Ground Command Reception and Telemetry Data Transmission >
- <Control Computer CPU, Sun Search Control Software, Timer Interrupt Signal>
- <Control Computer CPU, Sun Search Control Software, Mode Register Data>
- <Gyroscopes, Control Computer CPU, Gyro Communication>
- <Sun Sensors, Control Computer CPU, Sun Sensor Data Acquisition>
- <Three-axis Control Thrusters, Control Computer CPU, Thruster Data Acquisition>
-<Mode Register, Sun Search Control Software, Operating Mode Word>
-< Sun Search Control Software, Digital Tube, Telemetry Packaging>
-< Sun Search Control Software, Timer, Control Cycle>
-< Sun Search Control Software, Satellite, Attitude Angle and Angular Velocity>

