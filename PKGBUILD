pkgname=dmenu
pkgver=4.8
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

build() {
	cd /home/kn/src/dmenu
	make
}

package() {
	cd /home/kn/src/dmenu
	make DESTDIR="$pkgdir" PREFIX=/usr install
	install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
