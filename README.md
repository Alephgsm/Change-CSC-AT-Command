# How to change CSC of samsung device with AT Command
this toturial is suitable for developers also if you are technician you can use serial port utility for write AT Command and read response from device.

This solution is compatible with Android 9-10, and some device of Android 11.
Solution:
* boot device to normal mode.
* Enter the code *#0*# on dialer of device
 

# Programming:
You can implement this in any desired programming language, of course, if you are a technician, you don’t need to write a program, just use free software for working with serial port.
* use delay after every command, delpay count : 1000ms (1s)
* if you are using writeline of command , you dont need to use \r\n

* after dial *#0*# Open your serialport then follow this write items
**  ```AT+SWATD=0\r\n```
**  ```AT+ACTIVATE=0,0,0\r\n```
**  ```AT+SWATD=1\r\n ```

* in this step, you need country Code to changing
**  ``` AT+PRECONFG=2,YourCountryCode\r\n```
* Like can be
**  ``` AT+PRECONFG=2,THL\r\n```
* for rebooting device
**  ``` AT+CFUN=1,1\r\n```
