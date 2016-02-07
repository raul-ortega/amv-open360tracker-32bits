# amv-open360tracker-32bits 

This is the 32 bits versión of the "continuous 360 degree rotating antenna tracker system" for FPV. This proyect has been developed and maintained by users of the [FPV spanish community](http://www.aeromodelismovirtual.com/showthread.php?t=34530).

Please, we encourage you to read all the documentation before using this firmware in your devices, otherwhise they could be dammaged. In the wiki you'll find detailled information about how to install and configure it with success.

## Hardware paltform

This firmware has been developed for controllers based on STM32F series microprocessors, which fit the technical specifications of the popular NAZE32 flight controller. By now, it has been tested on the **Flip32** flight controller which incorporates the magnetometer, but it could work on other NAZE32 based boards like with external magnetometer.

# Features

* 360 degrees continous rotation.
* Multiprotocol.
* Protocol conversion and relay.
* Command line interface for configuration.
* Tilt easing

**360 DEGREE CONTINOUS ROTATION**

With this firmware you can move your antenna continually in a range of 360 degrees, without the need of moving back. Using an slipring and 360 degree servos, or normal servos modified to be able of doing it, the firware will give the orders for reaching the target in an acurate and fast way.

**MULTIPROTOCOL**

This firmware provides an **all in one anntena tracker controller system**, this means that it is able to work with several telemetry protocols without the the need of compiling and upload the firmware to the board each time you want to change from one to another.

These are the protocols that are supported:

- **MFD** 
- **DIRECT NMEA GPS Telemetry**
- **MAVLINK**
- **RVOSD**
- **FRSKY D**
- **FRSKY X (Smartport)**
- **LTM (Light Telemetry)**

El resto de protocolos soportados en la versión 8 bits están en fase de integración en esta nueva versión de 32bits.

**PROTOCOL CONVERSION AND FORWARDING**

With this firmware, you have the possibility to convert the input telemetry datato differents protocols formats, and fordward the frames to externals devices. 

- **MAVLINK** 
- **MFD**
- **FRSKY D**
- **FRSKY X (Smartport)**
- **HOTT**
- **LTM (Light Telemetry)**

Examples:

* Your aircrafat sends mavlink frames to the antenna tracker, and it converts and send the GPS position and altitude to the app Droid Planner. 
* The received telemetry data is converted to MFD protocol to manage an MFD antenna tracker. 

**COMMAND LINE INTERFACE**

Yo can configure and interact with the antenna tracker through a Command Line Interface (CLI) which will facilitate setting parameters using a remote console, as well as for example some app over Bluetooth.

**TILT EASING**

The tilt  movement has been improved by adding easing effects at the beginning and smoothing at the end. This will avoid damaging the tilt servo and other mechanisms when using heavy and larger antennas. This feature doesn't affect the accuracy and speed in the movements of the pan servo.
