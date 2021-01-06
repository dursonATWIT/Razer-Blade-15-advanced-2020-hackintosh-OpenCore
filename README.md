# Razer-Blade-15-advanced-2020-hackintosh-OpenCore

Tested with macOS 10.15.7 - 11.1

What doesn't work (yet):
1. Nvidia dGpu for obvious reasons, it has been disabled
2. Capslock light (known issue with razer)
3. SD Card reader
~~4. Intel wifi~~
~~5. Big Sur~~ Big Sur will lock to 60Hz but otherwise works

What does work that I've tested
1. Trackpad, disable force clicking
2. 300Hz (Catalina only, no idea why this is broken for Big Sur)
3. Audio (Switched from AppleALC to VoodooHDA, I am aware of the negative reputation of VoodooHDA, however in this particular case for this specific laptop until AppleALC is updated/I make a cusom layout, VoodooHDA is a better fit. Now with VoodooHDA internal speakers & headphone jack work with no distortion as well as built in and in line microphones. Automatic headphone/speaker switching is non function, the only fix would be switching back to AppleALC with a custom layout.
4. USB 3&C (thunderbolt not tested, USB drives appear as internal but still have the USB icon and are ejectable so oh well)
5. Webcam & webcam light
6. SSD (stock)
7. iGpu
8. Keyboard 
9. Brightness
10. Battery reporting 
11. Intel wifi now working but its very slow and unstable, not recommended
12. Intel Bluetooth
etc

"Guide" expects you to already more or less know what you're doing

--Pre install--
1. Copy efi folder to macOS install media's efi partition (use EFI Mounter 3.1)
2. Use OpenCore configurator to generate your own serial number
3. Disable secure boot in bios
4. Likely some other bios setting I forgot about idk

--Post install--
1. Navigate to System Preferences > Trackpad and disable Force Click or you will have a bad time
2. Copy efi folder to SSD's efi partition (use EFI Mounter 3.1 or OpenCore Configurator)
