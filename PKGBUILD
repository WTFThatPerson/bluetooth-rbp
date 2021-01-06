# Maintainer:

pkgname='bluetooth-rbp'
pkgver=0.1
pkgrel=1
pkgdesc='Bluetooth support for Raspberry Pi devices'
conflicts=('pi-bluetooth' 'bluetooth-raspberry')
arch=('armv6h' 'armv7h' 'aarch64')
license=('GPL')
url='http://wiki.archlinux.org/index.php/bluetooth'
#depends=('firmware-raspberrypi>=4' 'linux-raspberrypi>=4.14.59')
source=('90-pi-bluetooth.rules'
        '99-serial.rules'
        'btuart'
        'hciuart.service')
sha256sums=('087A87B75BD26993588FE7FB050B7440DC7427C889C977A07B3B76F11E5538D8'
            'B6677826060A3AE66C6EDB1211C04942FB2A20F7348F49B960F1B7B8B2A73B47'
            '8A14263A6F52AE3371279E4BBBBBF3608B01E0D7B898B455D1C53914154D6F7D'
            '704483A9534FA1BF84C7081A4846FA6D0300DC1968FDC3651FF2A123AAA9A11C')

package() {
  install -Dm644 ../90-pi-bluetooth.rules "${pkgdir}/usr/lib/udev/rules.d/90-pi-bluetooth.rules"
  install -Dm644 ../99-serial.rules "${pkgdir}/etc/udev/rules.d/99-serial.rules"
  install -Dm755 ../btuart "${pkgdir}/usr/bin/btuart"
  install -Dm644 ../hciuart.service "${pkgdir}/usr/lib/systemd/system/hciuart.service"
}
