# CG023
##**Firmware for CG023**

This is an alternate firmware for the Eachine CG023 quadcopter. It is a port of the Eachine H8 firmware, also by me ( silverxxx).

The quadcopter is based around the STM32F031 chip, Cortex M0 processor with 16K flash memory.

###Compiling:
Compile using MDK-ARM toolchain aka Keil uVision. A special version is available for stm32F0xx devices ( full free version ), but it's not necessary since the 32K limit of the free version is above the cpu's 16K. STM32 support may need to be installed using the "pack installer" 

###Radio protocol:
Current options are stock cg023 transmitter or H8 mini transmitter / devo. I recommend using the H8 protocol with Devo tx, as the cg protocol only allows approx 7 bits accuracy. Protocol is by default stock CG023 protocol.

###Accelerometer calibration:
Hold pitch stick down for 3 seconds, with throttle off. Needs to be done on a level surface. Saved so it only needs to be done once. You may need to use high rates in order to reach the treshold.

###Differences from H8 version:
 * rates have been integrated into protocol file, and depend on protocol abilities
 * the quadcopter rate ( in deg/sec) is no longer multiplied by 2, so it's the actual rate with devo.
 * linux version compiles above 16K, so it's not included.
 * acro only version can be compiled by enabling respective setting in config.h

###Installation and Support
Currently this port is covered by the H8 thread on rcgroups. Flashing is similar, except STM support is added using the pack installer.
http://www.rcgroups.com/forums/showthread.php?t=2512604

###History:


####26.03.16
* added pwm defines
* i2c speed improvement

####23.03.16
* some optimizations, etc

####20.03.16:
* dual mode added
* added alternate led "battery low 2" ( 3.3V )

####20.03.16:
* CG023 stock tx protocol added



