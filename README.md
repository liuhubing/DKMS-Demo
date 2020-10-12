# DKMS-Demo

## Ubuntu install command

sudo dkms add hello

sudo dkms install -m hello -v 0.1

## Ubuntu remove command
sudo dkms remove hello/0.1 --all

## Update All Installed Kernel Module
ls /var/lib/initramfs-tools | \
    sudo xargs -n1 /usr/lib/dkms/dkms_autoinstaller start

# Note. 
DKMS does not load auto load the module.

