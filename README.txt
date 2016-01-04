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

