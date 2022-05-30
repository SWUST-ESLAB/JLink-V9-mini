# JLink-V9-mini
this is a common tool for Cortex-M series MCU debugging , enjoy it!

**High Speed Flashing!!!** up to 12MHz

![A-side](https://github.com/SWUST-ESLAB/JLink-V9-mini/blob/main/2.Pics/Speed.png)

Have a look:

![A-side](https://github.com/SWUST-ESLAB/JLink-V9-mini/blob/main/2.Pics/jlink-front.png)

![B-side](https://github.com/SWUST-ESLAB/JLink-V9-mini/blob/main/2.Pics/jlink-back.png)

### How To Use

1. Clone this repository

   ```shell
   git clone https://github.com/SWUST-ESLAB/JLink-V9-mini.git
   ```

2. Modify the Pcb & Sch files as you wish!

   1. PCB assembled

3. Flash Bootloader

   - start J-Flash V6.34
   - open project : bootloader.jflash
   - click **connect** button at **Target** Tab
   - click **Production Programming** button at **Target** Tab
   - re-plug your JLINK and configure it in J-Link Commander
   - when you open J-Link commander , you will be asked for upload your firmware, click Yes
   - configure your J-Link via those commands

4. Configure your JLINK-V9

   ```
   Environment：JLINK V6.34
   ```

   Run the following commands in sequence under JLINK command

   ```shell
   Exec SetSN=29534567      ;Add SN v9.5
   Exec AddFeature GDB      ;Add GDB 
   Exec AddFeature RDI      ;Add RDI 
   Exec AddFeature FlashBP  ;Add FlashBP  
   Exec AddFeature FlashDL  ;Add FlashDL 
   Exec AddFeature JFlash   ;Add JFlash 
   Exec AddFeature RDDI     ;Add RDDI
   vcom enable              ;Enable VCOM
   ```

   other version of SN

   ```shell
   Exec SetSN=20281318 V9.2
   Exec SetSN=20381318 V9.3
   Exec SetSN=20481318 V9.4
   Exec SetSN=20581318 V9.5
   Exec SetSN=20681318 V9.6
   Exec SetSN=20781318 V9.7
   ```

   

