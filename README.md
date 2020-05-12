# bluetooth-rbp
Arch linux ARM Bluetooth firmware support for Raspberry Pi's include Raspberry Pi4. It supports aarch64 as well.

Clone repository into working directory and use makepkg in standard way, i.e. something like that:

cd ~
git clone https://github.com/WTFThatPerson/bluetooth-rbp.git
cd bluetooth-rbp
makepkg -si

Now You're ready to install bluez and bluez-utils and start using Bluetooth on Your device
