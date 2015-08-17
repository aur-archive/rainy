# Maintainer: Jonathan Csanyi <jdc@csanyi.ca>
pkgname=rainy
pkgver=0.5.0
pkgrel=2
pkgdesc="Synchronization server for use with Tomboy and other Tomboy-like clients"
arch=('i686' 'x86_64')
url="https://github.com/Dynalon/Rainy"
license=('AGPL')
groups=()
depends=('sqlite' 'mono-addins')
makedepends=()
optdepends=('screen: to run as a daemon')
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
source=('https://github.com/Dynalon/Rainy/releases/download/0.5.1/rainy-0.5.0.zip'
        'start-rainy' 'start-rainy-daemon')
noextract=()
md5sums=('1d57797036518d9430468092b6292f29'
         '30633fcee954b3c0de1117d01a0247bf'
         '84b9b70cf96b4dc8953d677fe5af850a')

package() {
  mkdir -p $pkgdir/usr/lib/rainy
  cp $srcdir/rainy-$pkgver/Rainy.exe* $pkgdir/usr/lib/rainy

  mkdir -p $pkgdir/usr/bin
  cp $srcdir/start-rainy* $pkgdir/usr/bin
  chmod a+x $pkgdir/usr/bin/start-rainy*

  mkdir -p $pkgdir/etc
  cp $srcdir/rainy-$pkgver/settings.conf $pkgdir/etc/rainy.conf
}

