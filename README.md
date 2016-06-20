#Partition for OpenWRT /Overlay
A simple script used to format an sd card with the first partition as the whole card and last partition 500MB on openwrt. Be sure to make it executable. This example is used to make the first partiton fat32 for windows use, and the second partiton ext4 for OpenWRT /overlay.

**Example**  
cd /tmp  
export LD_LIBRARY_PATH='/lib:/usr/lib:/tmp/lib:/tmp/usr/lib'  
opkg update && opkg install -d ram e2fsprogs mkdosfs fdisk  
wget http://druss.org/public/parts  
or  
wget https://raw.githubusercontent.com/TheExpertNoob/scripts/parts/parts  
chmod +x /tmp/parts  
./parts  
/tmp/usr/sbin/mkfs.vfat /dev/sda1  
/tmp/usr/sbin/mkfs.ext4 /dev/sda2  
