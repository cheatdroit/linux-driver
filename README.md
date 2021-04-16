# linux-driver


$ lsusb
Bus 001 Device 002: ID 0bda:f179 Realtek Semiconductor Corp. 802.11n
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 002 Device 002: ID 80ee:0021 VirtualBox USB Tablet
Bus 002 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

To install driver for 0bda:f179 Realtek Semiconductor Corp. 802.11n follow me

step 1:- install requirements
$ sudo apt-get install build-essential git dkms linux-headers-$(uname -r)

step 2:- clone git repo
$ sudo git clone https://github.com/kelebek333/rtl8188fu

step 3:- 
$ sudo dkms add ./rtl8188fu

step 4:- 
$ sudo dkms build rtl8188fu/1.0

step 5:- 
$ sudo dkms install rtl8188fu/1.0

step 6:- 
$ sudo cp ./rtl8188fu/firmware/rtl8188fufw.bin /lib/firmware/rtlwifi/

step 7:- 
$ reboot
