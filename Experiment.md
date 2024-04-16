# SUN
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
![Problem-diagram](https://github.com/nie0218/pictures/blob/main/Sun.png?raw=true)


# Digital Home
#Machine Domain
- Digital Home

#Given Domain
-Thermostats
-Humidistats
-Magnetic Alarm Contact Switches
-Security Sound and Light Alarms
-Appliances
-Web-ready Computers
-Cell Phones
-Broadband Internet Connection
-Power Switch
-User
-Contact Sensors
-Light Alarms
-Web Server

#Design Domain
-DH Gateway Device
-DH Home Web Server
-Environmental Controllers
-Home Database
-Sound Alarm Subsystem
-Light Alarm Subsystem
-Appliance Manager
-Digital Home Planner
-Report Generator

#Requirement Domain
-<Thermostat, Constraint, Monitoring and regulating temperature>
-<Thermostat, Reference, Providing current temperature reading>
-<Thermostat, Reference, Providing set point temperature>
-<Thermostat, Constraint, Sensitivity range between 14ºF and 104ºF>
-<Humidistat, Constraint, Monitoring and regulating humidity>
-<Humidistat, Reference, Providing current humidity reading>
-<Humidistat, Reference, Providing set point humidity>
-<Humidistat, Constraint, Setting humidity level from 30% to 60%>
-<Light Alarms, Constraint, Activating upon security breach>
-<Contact Sensors, Constraint, Monitoring entry through door or window>
-<Magnetic Alarm Contact Switches, Reference, Entry Monitoring>
-<Security Sound and Light Alarms, Reference, Security Breach Alert>
-<DH Gateway Device, Reference, Communication Center>
-<DH Gateway Device, Constraint, Connecting to broadband Internet>
-<Sensors, Reference, Value Reading>
-<Controllers, Reference, Value Sending>
-<Power Switch, Constraint, Monitoring state of appliance> 
-<Power Switch, Constraint, Changing state of appliance >
-<Power Switch, Constraint, Retain Manual State Setting>
-<Web Server, Constraint, Allowing remote control of DH System>
-<Web Server, Constraint, Serving as communication center>
-<Home Database, Constraint, Storing sensor values>
-<Home Database, Constraint, Storing controller values>
-<Appliance Manager, Constraint, Managing small appliances>
-<Appliance Manager, Constraint, Turning appliances on or off>
-<Digital Home Planner, Constraint, Directing preset home parameters>
-<Digital Home Planner, Constraint, Creating or modifying month plans>
-<Report Generator, Constraint, Generating management and control report>
-<Report Generator, Constraint, Providing month report>

#Phenomenon Sharing
-<Thermostats, DH Gateway Device, Wireless Communication>
-<Humidistats, DH Gateway Device, Wireless Communication>
-<Magnetic Alarm Contact Switches, Digital Home, Entry Monitoring>
-<Security Sound and Light Alarms, Digital Home, Security Breach Alert>
-<Digital Programmable Power Switches, Digital Home, Appliance State Monitoring>
-<Digital Programmable Power Switches, Digital Home, Appliance State Change>
-< Digital Home, Web Server, Web Control>
-< Digital Home, DH Gateway Device, Broadband Internet Connection>
-< Digital Home, Contact Sensors, Value Reading>
-< Environmental Controllers, DH Gateway Device, Value Sending>
-< Digital Home, User, Read Humidity at Humidistat Position>
-< Digital Home, User, Set Humidity Level>
-< DH Gateway Device, Home Database, Storing sensor values>
-< DH Gateway Device, Home Database, Storing controller values>
![Problem-diagram](https://github.com/nie0218/pictures/blob/main/Digital%20Home.png?raw=true)
