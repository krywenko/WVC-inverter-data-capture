# WVC-inverter-data-capture
Bash script  to display data from wireless  WVC inverters  from the serial modem
you will need to compile and install interceptty ( https://github.com/geoffmeyers/interceptty)

once interceptty is installed  the  command line  arguements  for WVC is wVC port inverter.list  modemID

example:
WVC /dev/ttyUSB0 inverters f3b67ac4

inverter.list  is a file created by you that contains the 4 character  ID of your inverters  each inverter ID on a new line 
example:
cb78
c794
c81f
... etc
 
 modemID is found on the back of your WVCmodem  it is 8 characters long 
 
if you want edit script to add in mqtt transmits or sending data directly to your data base  feel free to edict script
