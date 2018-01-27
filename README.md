forked.
it is for CY68013 and program the EEPROM to store VID/PID
software tool by Cypress.



#boring_logic
A 16-channel logic analyzer based on CY7C68013A MCU.

All hardware files are located in 'hardware' directry, including shematic, PCB, gerber files, and BOM.

R0A is an alpha version, and R01 is the final release.

In 'firmware' directry there are two EEPROM firmware files support Saleae Logic 8 and USBee AX Pro software. Firmwares are found from internet and only used for study.

To burn the firmware into EEPROM:

- Step1. Install driver in CypressTools\Drivers\CyLoad for CY7C68013A with blank EEPROM.
- Step2. Run CypressTools\bin\CyConsole.exe and open options --> EZ-USB Interface.
- Step3. Select S EEPROM and choose the .iic file.
- (Note: Download a CySuiteUSB tool with newest version from Cypress website if the tools in firmware directory are no longer compatible with your OS)

When you want to reburn the EEPROM, just disconnect the jumper and redo from Step1 to Step3.

#For Windows7:
Need to disable driver signature by pressing 'F8' key before loading the OS. Install CySuiteUSB and change the VID & PID numbers in INF driver file to match your device. Device VID & PID can be found in the windows device manager.
