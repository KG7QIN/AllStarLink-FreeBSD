The two files here are the patched versions of files found in the /usr/ports/misc/dahdi-kmod26 port.

To use these files, do the following:

cd /usr/ports/misc/dahdi-kmod26

make extract

make patch

copy the dahdi-base.c file in this repository to ./work/dahdi-freebsd-2.6.1-r10747/drivers/dahdi 

copy the kernel.h file in this repository to .//work/dahdi-freebsd-2.6.1-r10747/include/dahdi


make install


Make sure you rename the system.conf.sample file in /usr/local/etc/dahdi to system.conf


To start the dahdi drivers at boot, add the following line to your /etc/rc.conf:
dahdi_enable="YES"


Note that this driver has not yet been tested with AllStarLink on FreeBSD.  This is the intial version of the patched 
dahdi driver, and it may not work.  Once I have compiled and setup AllStarLink's Asterisk on FreeBSD, I will provide an update.

