# Problem-diagram
D. Jin, C. Wang and Z. Jin, "Automating Extraction of Problem Diagrams from Natural Language Requirement Documents," 2023 IEEE 31st International Requirements Engineering Conference Workshops (REW), Hannover, Germany, 2023, pp. 199-204, doi: 10.1109/REW57809.2023.00039.

下图为上述参考文献中通过设计神经网络模型从需求文档中提取建模元素，然后将它们组装成问题图。

该文献中使用sun search control system生成的问题图经过专家的讨论和评价，得出以下结论:

1.问题图中的A serial Port应该是外部设备的属性，所以不应该作为实体，其他节点都是正确的，所以正确性是15/16。

2. SS和DMC之间的共享现象没有被识别到，其他识别的现象都是正确的。

![Problem-diagram](https://user-images.githubusercontent.com/98217021/230363993-bd3ffacc-3f73-4f8b-84c1-98768e06dcab.png)


以下是通过使用我们设计的提示词从sun search control system需求文本中提取到的建模元素

#Machine Domain
- SunSearchControlSoftware

#Given Domain
- Gyroscopes
- SunSensors
- ThreeAxisControlThrusters
- DataManagementComputer
- GroundOperatorCommands
- SerialPort
- Analog-to-DigitalConverter (ADC)
- StoredCircuit
- Microcontroller80C32E
- Timer
- ControllerRegisters
- DigitalTube

#Design Domain
- ControlSystem
- SensorSubsystem
- ActuatorSubsystem
- ControllerSubsystem
- MainProgram
- InterruptServiceProgram

#Requirement Domain
- <Gyroscopes, Reference, Data Acquisition>
- <Gyroscopes, Constraint, Address for Sending Commands and Receiving Data>
- <SunSensors, Reference, Data Acquisition>
- <SunSensors, Constraint, Data Collection Format>
- <ThreeAxisControlThrusters, Reference, Control>
- <ThreeAxisControlThrusters, Constraint, Jetting Frequency>
- <ControlSystem, Reference, Composition>
- <ControlSystem, Constraint, Safety Criticality Level>
- <MainProgram, Reference, Initialization>
- <MainProgram, Constraint, Control Cycle>
- <InterruptServiceProgram, Reference, Timer Interrupt>
- <InterruptServiceProgram, Constraint, Timer Configuration>
- <Microcontroller80C32E, Reference, Core>
- <ControllerRegisters, Reference, Address>
- <ControllerRegisters, Constraint, Register Configuration>
- <DigitalTube, Reference, Telemetry Data Transmission>

#Phenomenon Sharing
- <SunSearchControlSoftware, Gyroscopes, Data Acquisition>
- <SunSearchControlSoftware, Gyroscopes, Address for Sending Commands and Receiving Data>
- <SunSearchControlSoftware, SunSensors, Data Acquisition>
- <SunSearchControlSoftware, SunSensors, Data Collection Format>
- <SunSearchControlSoftware, ThreeAxisControlThrusters, Control>
- <SunSearchControlSoftware, ThreeAxisControlThrusters, Jetting Frequency>
- <SunSearchControlSoftware, MainProgram, Initialization>
- <SunSearchControlSoftware, InterruptServiceProgram, Timer Interrupt>
- <SunSearchControlSoftware, Microcontroller80C32E, Core>
- <SunSearchControlSoftware, ControllerRegisters, Address>
- <SunSearchControlSoftware, DigitalTube, Telemetry Data Transmission>
