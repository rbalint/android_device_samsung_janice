android_device_samsung_janice
=============================

CyanogenMod 10.2 Device Tree for Samsung Galaxy S Advance (GT-I9070)

Supported variants:
  - GT-I9070 (INTL)

How to build:
=============

  repo init https://github.com/TeamCanjica/android.git -b cm-10.1
  
  repo sync -j32
  
  ./vendor/cm/get-prebuilts
  
  . build/envsetup.sh
  
      cd frameworks/av
      git fetch http://review.cyanogenmod.org/CyanogenMod/android_frameworks_av refs/changes/21/46421/3
      git cherry-pick FETCH_HEAD
      cd ../..
      cd system/core
      git fetch http://review.cyanogenmod.org/CyanogenMod/android_system_core refs/changes/32/45032/3
      git cherry-pick FETCH_HEAD
      cd ../..
  
  brunch janice
