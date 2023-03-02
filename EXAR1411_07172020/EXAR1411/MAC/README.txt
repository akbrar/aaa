10/31/13

This driver is for the XR21x141x USB UART product family: XR21v141x and XR21b1411 Standard x86-64 (32 and 64 bit universal) Mac driver.
The version number is 1.0.4.

----

This zip file contains the following 2 directories.

1) ExarUSBCDCACM_ver104_MacOS105_Obj : Driver files for MAC OSX 10.5

2) ExarUSBCDCACM_ver104_MacOS106_or_newer_Obj : Driver files for MAC OSX 10.6 and newer

----

Driver Installation:
Use an utility like "Kext Helper" to install ExarUSBCDCACM.kext or follow the manual steps given below.

Install 1: Manual Installation:
Copy "ExarUSBCDCACM.kext" to "/System/Library/Extensions" with root privileges
-        Open a terminal window and type
o        sudo cp -R /Users/yourusername/Desktop/ExarUSBCDCACM.kext /System/Library/Extensions
o        (Provide the root password in case it was not given earlier)

Install 2: 
Use "Kext Helper"
http://cheetha.net/

Note: You do not have to restart the system.

Once either one of the above driver installation is over, connect Exar's USB eval board to any of the USB port in the system.

The driver will automatically load and the serial ports will be enumerated. (For the device callout names, please check /dev folder or type "ls /dev/cu.*" in a terminal window. Exar ports will have "xrusbmodem****" string in them.) You can test these usb-uarts using any of the serial port applications.

----

For any questions, please send an e-mail request to uarttechsupport@exar.com. 

----

Changelog:

Ver 1.0.3 to 1.0.4 (October 2013):
- Changes only affect XR21B1411. Custom driver bit enabled for XR21B1411 so that Auto RTS/CTS HW flow control does not automatically get enabled when the XR21B1411 recceives a USB CDC request.
- Binary files for Mac OS X 10.5 (PowerPC and Intel processors) also included

Ver 1.0.2 to 1.0.3 (April 2012):
- No source code changes. The xcode project settings updated to build with the Mac OS X versions 10.6.7 and newer.
- Binary files provided for both 32-bit and 64-bit Mac OS based on Intel processor.

ver 1.0.1 to 1.0.2 (April 2011):
- Support for 32-bit Mac OS (based on Intel processor) only.