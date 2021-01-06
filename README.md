# bluetooth-rbp
Arch linux ARM Bluetooth firmware support for Raspberry Pi's include Raspberry Pi 4. It supports aarch64 as well.

Clone repository into working directory and use makepkg in standard way, i.e. something like that:

cd ~

git clone https://github.com/WTFThatPerson/bluetooth-rbp.git

cd bluetooth-rbp

makepkg -si

sudo reboot

sudo systemctl start hciuart

sudo systemctl enable hciuart

Now You're ready to install bluez and bluez-utils and start using Bluetooth on Your device

Please keep in mind, since kernel 5.4.50 this isn't needed anymore neither on Pi3 nor Pi4 because of native support of Bluetooth:
just put 

dtparam=krnbt=on

in /boot/config.txt and install bluez and bluez-utils is enough now
