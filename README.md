# linux-driver


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
