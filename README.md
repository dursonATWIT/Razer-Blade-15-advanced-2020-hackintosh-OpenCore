# Razer-Blade-15-advanced-2020-hackintosh-OpenCore

Tested with macOS 10.15.7 - 11.1

What doesn't work (yet):
1. Nvidia dGPU for obvious reasons, it has been disabled
2. C̶a̶p̶s̶l̶o̶c̶k̶ ̶l̶i̶g̶h̶t̶ ̶(̶k̶n̶o̶w̶n̶ ̶i̶s̶s̶u̶e̶ ̶w̶i̶t̶h̶ ̶r̶a̶z̶e̶r̶)̶ See bottom
3. SD Card reader (is a PCIe card reader not USB so will likely never work)
4. I̶n̶t̶e̶l̶ ̶w̶i̶f̶i̶
5. B̶i̶g̶ ̶S̶u̶r̶ Big Sur will lock to 60Hz but otherwise now works

What does work that I've tested
1. Trackpad, disable force clicking
2. 300Hz (Catalina only, no idea why this is broken for Big Sur)
3. Audio (Switched from AppleALC to VoodooHDA, I am aware of the negative reputation of VoodooHDA, however in this particular case for this specific laptop until AppleALC is updated/I make a cusom layout, VoodooHDA is a better fit. Now with VoodooHDA internal speakers & headphone jack work with no distortion as well as built in and in line microphones. Automatic headphone/speaker switching is non functional, the only fix would be switching back to AppleALC with a custom layout.)
4. USB 3&C (thunderbolt not tested, USB map completely fixed as of 1/11/21)
5. Webcam & webcam light
6. SSD (stock)
7. iGPU
8. Keyboard 
9. Brightness
10. Battery reporting 
11. Intel wifi now working but its very slow and unstable, not recommended. If you switch over to a new card remove the intel wifi kext first.
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

--Optional keyboard fix (requires 1/11/21 USB map fix)--
1. Download & install Karabiner Elements
2. Enable all requested permissions in preferences
3. Configure as shown (setting the function keys to media keys will not invert the keys so I recommend 2 profiles. I am working on color and fn control but don't count on it)
![screenshot 1](https://i.imgur.com/2fnqmBH.png)
![screenshot 2](https://i.imgur.com/BQnEPax.png)
![screenshot 3](https://i.imgur.com/1P5ErOH.png)
