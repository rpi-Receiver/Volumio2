# Volumio2

describes how to use the hat with Volumio2

prepare a SD Card wwith Volumio 2 https://volumio.org/get-started/

log in to volumio and install kernelsource

    volumio pull
    volumio kernelsource
copy KenelModules to volumios home

    sudo /home/volumio/rpi-receiver*/install.sh -c

add hardware to volumio:

    sudo nano /volumio/app/plugins/system_controller/i2s_dacs/dacs.json

add

    {"id":"rpi-Receiver","name":"rpi Receiver","alsaname":"rpiReceiver","overlay":"rpi-receiver","alsanum":"1","mixer":"Master","modules":"","script":"","eeprom_name":["rpiReceiver"],"needsreboot":"yes"},

at the propper place (alphabetical order)

select rpi Receiver as playback device and reboot.
