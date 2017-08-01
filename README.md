# ADC module manual
## First of all, you need to open your I2C function on your OS.
* sudo raspi-config 
## And then Install i2c-tools package.
* sudo apt-get update 
* sudo apt-get upgrade 
* sudo apt-get -y install i2c-tools
## Then git clone this code and configure your /boot/config.txt file.
* sudo vim.tiny /boot/config.txt 
 dtparam=i2c_arm=on
## Download the code and compile it and run it. 
* git clone https://github.com/geeekpi/adc.git
* cd adc/
* gcc -o adc_ntc_control_led  adc_ntc_control_led.c -lm -O3 
* sudo ./adc_ntc_control_led
---------
* gcc -o ntc_real_temperature  ntc_real_temperature.c -lm -O3 
* sudo ./ntc_real_temperature
## Reboot and try again.
