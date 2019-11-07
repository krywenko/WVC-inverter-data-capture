# WVC-inverter-data-capture
Bash script  to display data from wireless  WVC inverters  from the serial modem
you will need to compile and install interceptty ( https://github.com/geoffmeyers/interceptty) for openwrt precompoled binary can be found here  work on >=17 of open wrt 17 does not have jq  18 and up does bash grep, stty, bc, tac need to be installed on open wrt) 

once interceptty is installed  the  command line  arguements  for WVC is wVC port inverter.list  modemID

example:

WVC /dev/ttyUSB0 inverters f3b67ac4

inverter.list  is a file created by you that contains the 4 character  ID of your inverters  each inverter ID on a new line. it can be what ever name you want it to be. if you want to connect to multiple modems you can have  different list for each modem.


 modemID is found on the back of your WVCmodem  it is 8 characters long 
 
 the script is set for wvc 1200 series inverters     you can extract other series from the compressed file of inverters 
 
if you want edit script to add in mqtt transmits or sending data directly to your data base  feel free to edit script

if using  my version of energy monitor based on BPI R1 and/or Zero OPi  then uncomment  mosquitto_pub and it will automatcially written to  the localize  databases on these energy monitors ( you need to compole interceptty for them and install it) or use a secondary Zero OPi  that the  WVC modem is plugged into and  point the Mqtt pubish at BPi-R1 energy monitor  router 

https://github.com/krywenko/BPI-R1_Zigbee2mqtt-energymonitor-openwrt

https://github.com/krywenko/Zero-Orange-Pi--MQTT-openwrt


if you have issue  you can contact me here -- 

https://community.openenergymonitor.org/t/data-logging-wvc-gti-inverters-with-wireless-serial-modems/12302/2
