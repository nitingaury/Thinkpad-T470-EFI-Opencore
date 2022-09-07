# Thinkpad T470 20HE makes a stable Hackintosh machine! 
- Use Opencore Configurators associated to above mentioned versions
- EFI folder for Opencore Thinkpad T470 Hackintosh 20HE Touchscreen model
![Screenshot 2022-09-07 at 9 25 13 PM](https://user-images.githubusercontent.com/69560584/188924883-c74acf29-def2-4c3c-9fab-e0a58d379419.png)
![Screenshot 2022-09-07 at 9 30 48 PM](https://user-images.githubusercontent.com/69560584/188925504-c7a07be0-eeab-43bf-820f-fa56154550cc.png)
![Screenshot 2022-09-07 at 9 26 28 PM](https://user-images.githubusercontent.com/69560584/188924903-7df210e4-9bcf-499c-86a4-3455281f906a.png)
![Screenshot 2022-08-29 at 3 48 35 PM](https://user-images.githubusercontent.com/69560584/187180436-0cdcea01-6e9e-435e-903d-12f92a579514.png)
![Screenshot 2022-08-29 at 3 48 21 PM](https://user-images.githubusercontent.com/69560584/187180452-495b2e7e-7ec0-4802-9e55-7f7bbebd55dd.png)
![Screenshot 2022-08-29 at 3 48 58 PM](https://user-images.githubusercontent.com/69560584/187180478-a2127ca2-8491-4d4d-b5fb-8593d5725c29.png)
![Screenshot 2022-08-29 at 3 49 14 PM](https://user-images.githubusercontent.com/69560584/187180514-5c542690-3292-4244-895f-e4cb5e0a9502.png)
![Screenshot 2022-08-29 at 3 50 00 PM](https://user-images.githubusercontent.com/69560584/187180560-f14ac4c4-a774-48d6-947a-2307f13ea89f.png)

![prod-rc-lenovo-thinkpad-t470_Big](https://user-images.githubusercontent.com/69560584/173252878-b85074c5-dff4-46bc-986a-e200deb44b8b.png) ---> 99% working!

**Disclaimer**
- Hackintoshing may be dangerous and can damage your device and I am not responsible for bricked devices, dead devices, thermonuclear war, or you getting fired because your system failed. Please do some research if you have any concerns about hackintoshing before you proceed. YOU are choosing to make these changes to your system, and if you point the finger at me for messing up your device, I will laugh at you.

**MacOS versions**
- Mojave 
- Catalina
- Bigsur
- Monterey
- Ventura (Touchscreen is breaking sleep so has to disable it, waiting for release version)

**What's working?**

- Dual Battery (X220 Battery patch) 
- Fan control (Fan stops at low temp below 60 and starts working above 60 automatically, not to worry)
- Touchscreen (VoodooIC2HID)
- Power management (CPU friend data)
- Wifi (BCM94360NG)
- Bluetooth (BCM94360NG)
- USB C (only HDMI but no data transfer / Charging only)
- HDMI (No issues)
- Graphics HD 620 with acceleration (Metal Support)
- Apple HD Audio (ALC id=47)
- Sleep (works perfect!)
- wake works (no issues with resuming services like BT and wifi etc)
- SD Card slot
- Handoff and Continuity all features work as BCM94360ng has native support for macOS


**What's not working?**
- USB C data transfer
- Fingerprint reader (Will not work)

**DSDT and SSDT extraction and patching**
1. Extract your ACPI tables by using opencore debug version
2. Paste the root files in the respective folder locations in your system root
3. copy your ACPI Tables in the folder "ACPI-Tables)
4. execute "create_patched_DSDT.command" so you get the DSDT aml and dsl files
5. Now execute "install_ACPI_to_ESP.command" to generate all SSDT from samples
6. Copy .aml files to your ACPI folder which are needed only, refer to the updated efi folder for clarity. 

**Battery and power management performance and more perks!**
- Use itlwm/Airportitlwm for wifi and bluetooth firmware & injector kexts if you are on an intel wifi card, no kexts needed for bcm94360ng. //Note: for Monterey and above use bluetool fixup instead of bluetooth injector kext.//
- Temperature management is decent and backup depends on how you use and on what task the system is running
- Sleep works fine with approx 2%-4% for 6 Hrs loss (Which is neglegible)
- Enable HiDpi by using this beautiful tool at "https://github.com/xzhih/one-key-hidpi", Set 2048x1152x32 [16:9] as best screen resolution using RDM(Retina Display Menu) from here -> "https://github.com/avibrazil/RDM".
- If you are using FakeSMC fan rpm shows up natively, if you are using VirtualSMC then use YogaSMC.kext for fan rpm.

**My sincere thanks to**
- Rehabman -> DSDT Patches (Used MaciASL for patching and compiling)
- Tluck's Repository, Great work done there!
- Tonymac86 -> DSDT Guide
- Acidanthera -> Kexts
- Open Core Team -> EFI Creation and Troubleshooting
- Proper Tree -> Workarounds and EFI editing
- Corpnewt -> USB Mapping kext
- Team Voodoo -> Keyboard, mouse and touchscreen
- Chris1111 -> Theming
- and the entire community for inspiring me!

I was into Hackintoshing since 14 years and its was always fun to try something like this! 

--------------------------------------------------------------------------------------------- (Print : End)
