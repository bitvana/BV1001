## Device Tree Overlay Install

Compile the .dts file with the following command
```
# dtc -O dtb -o BITVANA-XBC1-00A0.dtbo -b 0 -@ BITVANA-XBC1.dts
```
then copy the resulting .dtbo file to /lib/firmware (as root)
```
# cp BITVANA-XBC1-00A0.dtbo /lib/firmware
```
reboot the system and check if the overlay loaded
```
root@beaglebone:~# cat /sys/devices/platform/bone_capemgr/slots
 0: P---L-   0 Bitvana XBee Cape 1,00A0,Bitvana LLC,BITVANA-XBC1
 1: PF----  -1
 2: PF----  -1
 3: PF----  -1
```
If you have any questions please contact us at support@bitvana.com