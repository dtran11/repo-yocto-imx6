Yocto Setup Guide
-----------------

1) Download the script "yocto-setup"

2) Type: chmod +x yocto-setup

3) Type: ./yocto-setup

3) Wait for repo to download the yocto related repositories

4) Yocto build environment is now at ~/poky



Yocto Build
-----------

1) Type: source ~/poky/oe-init-build-env

2) Type: export MACHINE="${MY_MACHINE}"	
	
3) Type: bitbake console-image         OR
         bitbake core-image-sato

4) Wait for image to build (first time will take several hours)

4) Images are at "~/poky/build/tmp/deploy/images


IMX6 SD Partition
-----------------

SPL should be written at offset 1KB

   sudo dd if=SPL of=/dev/sdX bs=1K seek=1
   
U-Boot should be written with 69 blocks offset

   sudo dd if=u-boot.img of=/dev/sdX bs=1K seek=69
   
Create a BOOT FAT32 partition with offset 4MB of size 8MB

Create EXT4 partition after the BOOT partition

