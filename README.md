# Thinkpad T470 (Opencore version 0.7.5 and 0.8.2)
- Use Opencore Configurators associated to above mentioned versions
 EFI folder for Opencore Thinkpad T470 Hackintosh, for educational purposes only!
 
 ![Screenshot 2022-06-27 at 22 59 05](https://user-images.githubusercontent.com/69560584/176019544-e079d93f-f2db-4881-8b67-75cd78114ea6.png)
![Screenshot 2022-06-14 at 5 00 00 AM](https://user-images.githubusercontent.com/69560584/176019662-387c68d7-aa76-432b-b654-4030dffcc359.png)
![Screenshot 2022-06-13 at 1 47 10 AM](https://user-images.githubusercontent.com/69560584/176019745-6d6d80ca-a2dd-47ab-ac05-16fada6ca193.png)
 
![prod-rc-lenovo-thinkpad-t470_Big](https://user-images.githubusercontent.com/69560584/173252878-b85074c5-dff4-46bc-986a-e200deb44b8b.png) ---> 99% working!

**Disclaimer **
- Hackintoshing may be dangerous and can damage your device and I am not responsible for bricked devices, dead devices, thermonuclear war, or you getting fired because your system failed. Please do some research if you have any concerns about hackintoshing before you proceed. YOU are choosing to make these changes to your system, and if you point the finger at me for messing up your device, I will laugh at you.

**MacOS versions **
- Bigsur
- Monterey
- Ventura

**What's working? **

- Dual Battery (DSDT/SSDT) 
- Touchscreen (VoodooIC2HID)
- Power management (CPU friend data)
- Wifi (Airportitlwm)
- Bluetooth (Intel Bluetooth firmware)
- USB C port (no data transfer / Charging only)
- HDMI (No issues)
- Graphics HD 620 with acceleration
- Apple HD Audio (ALC id=47)
- Sleep (on AC and off AC)
- wake works (no issues with resuming services like BT and wifi etc)
- SD Card port


**What's not working? **
- USB C data transfer
- Thunderbolt and 
- Fingerprint reader

**Battery and power management performance **
- Generate CPU Data provider kext and CPU-data-friend.aml by using https://github.com/corpnewt/CPUFriendFriend , Please note you need to generate these everytime you update the OS to next version, use the lowest frequency by "08" for 800 MHz.
- Battery works efficiently and gives a 4.5 hr approx, CPU friend data provider kext performing fine with base frequency as 800 MHz having said average of 1.6 GHz and the peak is 3.5 GHz. 
- Temperature management is decent and backup depends on how you use and on what task the system is running
- Sleep works fine with approx 2%-4% for 6 Hrs loss (Which is neglegible)

**My sincere thanks to **
- Olarila - MaLd0n
- Open Core Team
- Proper Tree
- TonymacX86
- Insanelymac
- Rehabman
- Team Voodoo
- and the entire community for inspiring me!

I was into Hackintoshing since 14 years and its was always fun to try something like this! 

--------------------------------------------------------------------------------------------- (Print : End)
