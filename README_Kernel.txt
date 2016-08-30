################################################################################
HOW TO BUILD KERNEL FOR SM-J700F_MEA_MM_TUR

1. How to Build
	- get Toolchain
	download and install aarch64-linux-android-4.9 toolchain for ARM EABI.
	Extract kernel source and move into the top directory.

	$ make ARCH=arm64 j7elte_defconfig
	$ make ARCH=arm64 -j64
	
	
2. Output files
	- Kernel : Kernel/arch/arm/boot/zImage
	- module : Kernel/drivers/*/*.ko
	
3. How to Clean	
    $ make clean
	
4. How to make .tar binary for downloading into target.
	- change current directory to Kernel/arch/arm/boot
	- type following command
	$ tar cvf SM-J700F_MEA_MM_TUR.tar zImage
#################################################################################