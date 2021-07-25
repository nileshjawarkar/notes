# Install guest aditions

## Install guest aditions - Centos
- Install some preqs
	- `yum -y install epel-release`
	- `yum -y update`
	- `yum install make gcc kernel-headers kernel-devel perl dkms bzip2`
	- and restart the VM
- Insert guest aditions ISO
	- ![](/home/nilesh/Tmp/insert_g_cd.png)
	- This ISO will be available at
		- `/dev/disk/by-lable/VBox*`
	- Mount this at \mnt\iso
	- cd to /mnt\iso and run 
		- ./VBoxLinuxAdditions.run 
		- 
## Install guest aditions - Debian
- Install some preqs
	- sudo apt update
	- sudo apt install build-essential dkms linux-headers-$(uname -r)
- Rest things same as centos

## Install guest additions on Arch linux
- pacman -Sy virtualbox-guest-utils

## Check guest aditions
- lsmod | grep vboxguest
