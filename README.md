# The Thinkpad T470 20HE makes a stable Hackintosh machine! 

![lenovo T470 github](https://user-images.githubusercontent.com/69560584/189785204-1f684515-7708-4a69-ae59-a0161249cce4.png)
![Screenshot 2022-09-13 at 6 00 02 AM](https://user-images.githubusercontent.com/69560584/189782384-6f9df794-3fac-48b6-9e40-c135c030c8f5.png)
![Screenshot 2022-09-13 at 5 55 21 AM](https://user-images.githubusercontent.com/69560584/189782400-99d6fef9-711e-41a6-a687-c9dc68210f5d.png)
![Screenshot 2022-09-13 at 5 54 45 AM](https://user-images.githubusercontent.com/69560584/189782402-60d9235a-bb02-4887-8e1d-4b8764056cce.png)
![Screenshot 2022-09-13 at 5 54 37 AM](https://user-images.githubusercontent.com/69560584/189782404-569861de-ad6c-4695-8f87-2b967549b6db.png)
![Screenshot 2022-09-21 at 16 15 16](https://user-images.githubusercontent.com/69560584/191485495-6ea807cd-acee-4700-b586-dc1f4321bc89.png)

**Disclaimer**
- Hackintoshing may be dangerous and can damage your device and I am not responsible for bricked devices, dead devices, thermonuclear war, or you getting fired because your system failed. Please do some research if you have any concerns about hackintoshing before you proceed. YOU are choosing to make these changes to your system, and if you point the finger at me for messing up your device, I will laugh at you.

**MacOS versions**
- Mojave 
- Catalina
- Bigsur
- Monterey
- Ventura 

**What's working?**

- Dual Battery (X220 Battery patch) 
- All function keys working with yoga SMC
- Graphics HD 620 with acceleration (Metal 3 Supported) - [VRAM = 4096MB]
- Fan control (Fan stops at low temp below 60 and starts working above 60 automatically, not to worry)
- Touchscreen (VoodooI2C)
- Power management (CPU friend data)
- Wifi (BCM94360NG)
- Bluetooth (BCM94360NG)
- USB C (only HDMI but no data transfer / Charging only)
- HDMI (No issues)
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
- Disable hibernation, since it doesn't work properly on hackintoshes
```
sudo pmset autopoweroff 0
sudo pmset powernap 0
sudo pmset standby 0
sudo pmset proximitywake 0
sudo pmset tcpkeepalive 0
```
- Use itlwm/Airportitlwm for wifi and bluetooth firmware & injector kexts if you are on an intel wifi card, no kexts needed for bcm94360ng. //Note: for Monterey and above use bluetool fixup instead of bluetooth injector kext.//
- Temperature management is decent and backup depends on how you use and on what task the system is running
- Sleep works fine with approx 2%-4% for 6 Hrs loss (Which is neglegible)
- Enable HiDpi by using this beautiful tool at "https://github.com/xzhih/one-key-hidpi", Set 2048x1152x32 [16:9] as best screen resolution using RDM(Retina Display Menu) from here -> "https://github.com/avibrazil/RDM".
- If you are using FakeSMC fan rpm shows up natively, if you are using VirtualSMC then use YogaSMC.kext for fan rpm.
- unifiedmem values for vram 
```
00000040 = 1024MB
00000060 = 1536MB
00000080 = 2048MB
000000A0 = 2560MB
000000C0 = 3072MB
000000E0 = 3584MB
FFFFFFFF = 4096MB
```
**Next into undervolting:**


## My sincere thanks to**

- [Acidanthera](https://github.com/acidanthera)
- [Dortania OC guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [Rehabman's battery patch guide](https://www.tonymacx86.com/threads/guide-how-to-patch-dsdt-for-working-battery-status.116102/) and [Rehabman's ACPI hotpatching guide](https://www.tonymacx86.com/threads/guide-using-clover-to-hotpatch-acpi.200137/)
- [CorpNewt's tools](https://github.com/corpnewt)
- [VoodooRMI](https://github.com/VoodooSMBus/VoodooRMI)
- [YogaSMC](https://github.com/zhen-zen/YogaSMC)
- [Daliansky's OC-little repo](https://github.com/daliansky/OC-little)
- and the entire community for inspiring me!

I was into Hackintoshing since 14 years and its was always fun to try something like this! 

--------------------------------------------------------------------------------------------- (Print : End)
