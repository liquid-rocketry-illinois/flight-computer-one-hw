# Flight Computer One "Electric Angel"
KiCad PCB repository for Electric Angel, LRI's first fully featured flight computer. An evolution of the Flight Computer Lite (nicknamed Digital Tripper), it integrates several great new features, like a packet radio, CAN FD, hardware floating-point acceleration, pyro channels, servo controls and more! Electric Angel can do many things: it can fly model rockets with active controls, act as a wireless comms link for liquid powertrain operation, or maybe someday, both at the same time. It can also log data at a rate exceeding that of Digital Tripper.

Control and comms code written for Digital Tripper is directly portable due to Raspberry Pi Silicon architecural similarities. Obviously the board layouts are not identical, so the relevant changes for interfacing with the other chips will need to be made to any code written for DT.

Electric Angel is a 50mm x 100mm rectangle and is designed to fit longitudinally in an avionics bay. Its physical design is inspired by the TeleMega series of altimeters.

Ingredients:
* The "brain", a Raspberry Pi Silicon RP2350B
* Various digital sensors
    * TDK InvenSense ICM-42688-P high-accuracy 6DoF IMU
    * Bosch BMI088 6DoF IMU for backup and a higher (24 g) acceleration limit
    * STmicroelectronics LIS2MDL 3-axis magnetometer
    * TE Connectivity MS5611 barometer/altimeter
    * Sensirion SHT40 for ambient temperature and humidity
    * u-blox MAX-M10S GNSS receiver and a u.FL antenna connector
* A 915MHz LoRa radio module and a u.FL antenna connector (Ai-Thinker RA-01H)
* A push-push microSD card slot for vibration-resistant datalogging
* A piezo buzzer for providing auditory feedback
* A USB Type-C 2.0 port for programming and serial communication
* An XT60 battery connector (supports 2S or 3S lithium battery packs)
* A power monitor IC
* A power mux for utilizing battery or USB power
* A 3.3V buck converter
