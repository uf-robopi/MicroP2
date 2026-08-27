### TivaWare SDK Download
- For downloading the **TivaWare SDK**, please make a TI account and download it from the following link: 
[ti.com/tool/SW-TM4C](https://www.ti.com/tool/SW-TM4C) 
- If you have a Linux device, download the .exe and then change the extension to .zip. Afterwards, unarchive it and place it in a memorable location so your CCS projects can reference it.

### Resolving issues with linker
- add the driverlib.lib file to the include options on your CCS
-   can be found in this file path on windows C:\ti\TivaWare_C_Series-2.2.0.295\driverlib\ccs\Debug

### Resolving issues with "uartstdio not found"
- move the uartstdio.h and uartstdio.c files into driverlib
-   can be found in this file path C:\ti\TivaWare_C_Series-2.2.0.295\driverlib



### Common Flashing Issue - Cortex M4: Error Connecting to the Target
The m4 not connecting is an issue that usually arises whenever attempting to flash the code onto the board. This happens due to the Stellaris drivers not being implemented properly for recognizing the device. To fix this, download the drivers from [this link](https://www.ti.com/tool/STELLARIS_ICDI_DRIVERS), then navigate to your Device Manager. Under "Other Devices", you should see "In-Circuit Debug Interface" or something similar. Right click the device, select update driver, browse my computer for drivers, then browse to the folder with the stellaris drivers. Click next, and the drivers should be installed!


If that does not fix your problem, try the below steps

- There is a sliding switch on the launchpad next tot he microUSB port, flip the switch, that switch turns the board on and off
- If that doesn't work, then click on the project you're working on, and go to properties (alt+enter)
      -From there go to the debug tab, open "Auto Run and Launch Options", and make sure under "Launch Options" that the setting "Connect to the target on debugger startup" is checked
      - <img width="800" height="523" alt="image" src="https://github.com/user-attachments/assets/76123ae1-517b-4586-a2c7-361c89f9bb63" />



