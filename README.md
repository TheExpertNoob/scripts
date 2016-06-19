A simple script used to format an sd card with the first partition as the whole card and last partition 500MB on openwrt. Be sure to make it executable.

**Example**  
cd /tmp  
export LD_LIBRARY_PATH='/lib:/usr/lib:/tmp/lib:/tmp/usr/lib'  
opkg update && opkg install -d ram e2fsprogs mkdosfs fdisk  
wget http://druss.org/public/parts  
chmod +x /tmp/parts  
./parts  
/tmp/usr/sbin/mkfs.vfat /dev/sda1  
/tmp/usr/sbin/mkfs.ext4 /dev/sda2  
