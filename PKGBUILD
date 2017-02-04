pkgname=("routewatcher")
pkgver=1.0.0
pkgrel=1
pkgdesc="A tool to copy addresses into the routing table"
arch=("any")
url="https://github.com/hackyourlife/routewatcher"
license=("Custom")
depends=("python" "python-dnspython")
backup=(etc/routewatcher-domains.lst)
source=(routewatcher domains.lst routewatcher.service)
md5sums=('c505cfbe83e59fd25e341a3373d01ade'
         '757b1635bb6a2ad61ca20b5c1f227f76'
         '402e52aa75c23bf8bc07bc2922edd766')

package() {
  cd "$srcdir"
  mkdir -p "$pkgdir/etc"
  mkdir -p "$pkgdir/etc/systemd/system"
  mkdir -p "$pkgdir/usr/bin"
  install -m755 routewatcher "$pkgdir/usr/bin/routewatcher"
  install -m644 routewatcher.service "$pkgdir/etc/systemd/system/routewatcher.service"
  install -m644 domains.lst "$pkgdir/etc/routewatcher-domains.lst"
}

# vim:set ts=2 sw=2 et:
