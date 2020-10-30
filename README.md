# Razer-Blade-15-advanced-2020-hackintosh-OpenCore

Tested with macOS 10.15.7

What doesn't work (yet):
1. dGpu for obvious reasons, it has been disabled
2. Intel wifi
3. SD Card reader
4. Capslock light (known issue with razer)

What does work that I've tested
1. Trackpad, disable force clicking
2. 300Hz
3. Audio
4. Usb 3&C (thunderbolt not tested)
5. Webcam & webcam light
6. SSD (stock)
7. iGpu
8. Keyboard (ALT key is replaced by the WIN key for whatever reason, bugs me)
9. Brightness
10. Battery reporting (seems iffy with the % so far, kext just might need time though)
etc

"Guide" expects you to already more or less know what you're doing

--Pre install--
1. Copy efi folder to macOS install media's efi partition (use EFI Mounter 3.1)
2. Use OpenCore configurator to generate your own serial number
3. Disable secure boot in bios
4. Likely some other bios setting I forgot about idk

--Post install--
1. Navigate to System Preferences > Trackpad and disable Force Click or you will have a bad time
2. Copy efi folder to SSD's efi partition (use EFI Mounter 3.1)
