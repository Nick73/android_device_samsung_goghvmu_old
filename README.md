Copyright 2013 - The CyanogenMod Project

Device configuration for Samsung Galaxy Victory (Virgin Mobile model).

WORK IN PROGRESS. WILL EAT YOUR CAT.


CyanogenMod for goghvmu
=======================

Getting Started
---------------

To get started with Android/CyanogenMod, you'll need to set up your [Ubuntu Environment](http://vmobi.us/?page_id=8).
Once completed you will need to initialize your local repository using the CyanogenMod trees, use a command like this:

    repo init -u git://github.com/CyanogenMod/android.git -b jellybean

Then to sync up:

    repo sync

Device / Vendor / Kernel Files
------------------------------

Once you are synced run the following commands inside the source folder to download the needed files

Download the device files

    git clone git://github.com/vmobi-victory/android_device_samsung_goghvmu.git -b jellybean device/samsung/goghvmu

Download the vendor files

    git clone git://github.com/vmobi-victory/android_vendor_samsung_goghvmu.git -b jellybean vendor/samsung/goghvmu

Download the common files

    git clone git://github.com/vmobi-victory/android_device_samsung_gogh-common.git -b jellybean device/samsung/gogh-common

Download the common qcom files

    git clone git://github.com/CyanogenMod/android_device_samsung_qcom-common.git -b jellybean device/samsung/qcom-common

Download the kernel source

    git clone git://github.com/vmobi-victory/android_kernel_samsung_goghvmu.git kernel/samsung/goghvmu

Time to configure the CyanogenMod prebuilts

    vendor/cm/get-prebuilts 

Building
--------

Once the device and vendor files are set up, it is now time to build

    . build/envsetup.sh && brunch goghvmu -j#

The # stands for the ammount of threads to use per cpu core. Google recommends two threads 
per core, so if you have eight cores on your system you would use -j16.
