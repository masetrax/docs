# OpenBSD Tips and Tricks

## Improve memory limit to avoid core dumps

`su`
`usermod -G staff YOUR_USERNAME`
edit `/etc/login.conf`
Under staff, edit `datasize` to `datasize-cur=4096M:\`

## Setup user mounting of external drives using doas
The following commands (as root) will add the needed lines to doas.conf

`echo "permit nopass keith as root cmd mount" >> /etc/doas.conf
echo "permit nopass keith as root cmd umount" >> /etc/doas.conf
echo "permit nopass keith as root cmd ntfs-3g" >> /etc/doas.conf`

Mounting a USB stick to ~/usb as user looks like this:

`mkdir ~/usb
dmesg | grep sd1
sd1 at scsibus4 targ 1 lun 0: <, USB DISK 2.0, PMAP> removable serial. numbers
doas mount /dev/sd1i ~/usb
ls ~/usb
music
planner.pdf`

With this VFAT formatted USB stick plugged in, I can mount my NTFS formatted backup drive to ~/backup like this:

`mkdir ~/backup
dmesg | grep sd2 
sd2 at scsibus5 targ 1 lun 0: <WD, Elements 10B8, 1012> serial. numbers
ls ~/backup
doas ntfs-3g /dev/sd2i ~/backup
ls ~/backup
Music                      System Volume Information
Pix                        X220`

Below are the commands for unmounting both drives:

`doas umount ~/usb
doas umount ~/backup
ls usb
ls backup`
