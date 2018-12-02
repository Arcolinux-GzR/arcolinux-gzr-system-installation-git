# Maintainer: Erik Dubois <erik.dubois@gmail.com>
pkgname=arcolinux-gzr-system-installation-git
_pkgname=arcolinux-gzr-system-installation
_destname1="/etc/xdg/autostart"
_destname2="/usr/share/applications"
_licensedir="/usr/share/arcolinux/licenses/"
pkgver=18.12
pkgrel=1
pkgdesc="Installation files for Arco-GzR"
arch=('any')
url="https://github.com/Arcolinux-GzR/arcolinux-gzr-system-installation"
license=('GPL3')
makedepends=('git')
depends=()
provides=("${pkgname}")
options=( !strip !emptydirs )
source=(${pkgname}::"git+https://github.com/Arcolinux-GzR/${_pkgname}")
sha256sums=('SKIP')
package() {
  install -dm755 "$pkgdir/$_licensedir/$_pkgname"
  install -m644 "$srcdir/$pkgname/LICENSE" "$pkgdir/$_licensedir/$_pkgname"

  install -dm755 "$pkgdir$_destname1"
  install -m644 "$srcdir/$pkgname/$_destname1/"* "$pkgdir$_destname1"

  install -dm755 "$pkgdir$_destname2"
  install -m644 "$srcdir/$pkgname/$_destname2/"* "$pkgdir$_destname2"
}
