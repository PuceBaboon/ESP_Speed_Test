# ESP_Speed_Test

This is Ray Burnette's ESP8266 version of Reinhold P. Weicker's Dhrystone speed test, modified very slightly to provide some indication of the speed difference between running the ESP8266 at 80MHz and 160MHz.

I wouldn't recommend putting too much reliance on the actual figures it produces, but it does show a difference between the two different clock rates.


## Dynamic

The Speed_Test_Dynamic.ino file will alternat the clock rate between 80MHz and 160MHz on successive iterations using the `system_update_cpu_freq()` system call.  Note that the system call will override any platformio.ini settings you may have.


## Static

The Speed_Test_Static.ini file is closer to Ray's original and simply loops at whatever the system clock frequency is set at in the platformio.ini file.  You can use this to ensure that your compile time setting is actually affecting the system clock.


## PlatformIO

The platformio.ini_example file simply shows the PlatformIO syntax for setting the ESP8266 clock speed at compile time.


