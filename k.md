# Hackintosh on alienware
 Basic requirement
 - Usb 8gb or more
 - Second laptop
 - Windows or mac os x
 - Good internet connection
 - My guide and My files
 ## Now follow my guide
 - Download mac os x with mac app store and UseCreateMedia installation method more detail on [apple website](https://support.apple.com/en-us/HT201372).
 - After creating bootable usb Install clover in it ; [Clover]().
 - Then copy paste my config.plist and boot it .
 - most probably it will not you are happily report me !.
 - Installation process is easy but for dual/triple boot make +1 partition. Eg if you want triple boot you have to make 4 partition 1 extra because if you want transfer files between os ; So it is more convenient.
 - After installation now main task come which is called **post installation**.
 - I use Hackintosh vietnam tool which is more convenient for use by finding drivers by every site but the main problem some drivers are not update like Realtek Usb Wifi and many other which you can update by own but if you want which drivers used I will give you whole list.
 - Now after post installation, most of you think installation is complete but not actually there are many things not working like Sleep, All usb ports etc.
 - Now for this You have to extract DSDT file , 'I prefer use linux for this' Now it is upto you which method you prefer
 - ### Extraction DSDT and patching
 - -   There are 2 major method one is clover method and other linux method
  - Clover method is quite easy just press F4 on clover screen with FN key or without it will extracted your acpi files I face 2 times that My acpi are either corrupted or duplicate and give me error when I am doing disassembling
   - For linux method which I like and prefer it is easy to just make bootable Usb of Ubuntu (Using rufus)
    - open terminal and paste this command
      - `sudo cp -R /sys/firmware/acpi/tables DEST`
      - Now you will see a DEST Folder in your home folder , you need a Usb drive which is formatted in FAT-32 drive ; Now back to DEST folder, it is locked just put this command
      - `Sudo nautilus`
      - Copy paste into FAT-32 drive and you successfully extracted Your ACPI files
      - **Disassembling part**
      - For this you will need IASL and you can download from this [site](https://bitbucket.org/RehabMan/acpica/downloads)
      - Paste into /Usr/Bin
      - Now I am assuming that you Extracted Your Acpi files From Linux and paste into Downloads Folder
      - In Terminal folder
      - `cd ~/Downloads/DEST`
      - `iasl -da -dl DSDT SSDT*`
      - Now you will get Exctracted DSDT, SSDT file in .dsl format
      - Now you need these [MaciASL](https://github.com/RehabMan/OS-X-MaciASL-patchmatic)
        [Laptop Patches](https://github.com/RehabMan/Laptop-DSDT-Patch)
