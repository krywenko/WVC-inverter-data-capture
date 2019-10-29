# WVC-inverter-data-capture
Bash script  to display data from wireless  WVC inverters  from the serial modem
you will need to compile and install interceptty ( https://github.com/geoffmeyers/interceptty)

once interceptty is installed  the  command line  arguements  for WVC is wVC port inverter.list  modemID

example:

WVC /dev/ttyUSB0 inverters f3b67ac4

inverter.list  is a file created by you that contains the 4 character  ID of your inverters  each inverter ID on a new line. it can be what ever name you want it to be. if you want to connect to multiple modems you can have  different list for each modem.


 modemID is found on the back of your WVCmodem  it is 8 characters long 
 
 the script is set for wvc 1200 series inverters     you can extract other series from the compressed file of inverters 
 
if you want edit script to add in mqtt transmits or sending data directly to your data base  feel free to edit script
