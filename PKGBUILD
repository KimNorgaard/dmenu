pkgname=dmenu-kn
pkgver=5.2
pkgrel=1
pkgdesc="My own fork of dmenu"
url="https://tools.suckless.org/dmenu/"
arch=('x86_64')
license=('MIT')
license=('GPL')
depends=('libxinerama' 'libxft')
provides=(dmenu)
conflicts=(dmenu)

source=()
md5sums=()

builddir=$(pwd)

build() {
  cd $builddir
	make
}

package() {
  cd $builddir
	make DESTDIR="$pkgdir" PREFIX=/usr install
	install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
