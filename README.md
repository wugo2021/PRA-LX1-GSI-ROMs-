# PRA-LX1-GSI-ROMs-

system.img gsi for pra-lx1
 Download
All target builds

About

crDRom11 is a project which based on crDroid 7.x with Andy Yan's and phhusson's Treble GSI patches. Built with some Andy's patches & recommendations, also even without "ALLOW_MISSING_DEPENDENCIES=true" flag. And system can run with SELinux enforced state, as original Phh AOSP GSI. Fully compatible with PHH-Treble patches. Has dynamic root which can be activated/deactivated without reboot - 'su' binary and SuperUser app (can works on all devices even with system read-only). Also has dynamic SafetyNet helper (but it compatible with not all devices), users have four ways to pass SafetyNet: a. just enable SafetyNet option (recommended) b. disable SafetyNet and enable "Spoof Pixel 5" then reboot c. enable both options and reboot d. mount system as RW and create empty file /system/phh/secure (legacy method)

Changes
crDRom R 22.03.30

March 2022 SPL
added blockdev calls for RW system, this can be fix read-write mounting for some devices and otherwise can broke boot on some ones (need test)
backported changes from device_phh_treble: Add Samsung way to grab ro.telephony.default_network, Change fingerprint manifest grep, Samsung: keep user's recovery, Fix Play Services crashing on Galaxy S21 Ultra, Fix bluetooth audio Motorola 'liber', Disable fingerprint gestures for Stylo 7 4G variant
backported from frameworks_av: fixup! Not all sources in route are valid
backported from system_core: Let system override ro.apex.updatable
patch for Zygote: fix an issue when empty the usap pool
restored SuperUser legacy app
reworked 'daisy' overlay
