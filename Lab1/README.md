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



