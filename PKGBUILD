# Maintainer: Aditya Gupta <ag15035 at gmail dot com>
pkgname=run-cpp-git
pkgver=r3.efd50dd
pkgrel=1
pkgdesc="A simpler shorter way to Compile AND Run a .cpp file"
arch=('x86_64')
url="https://github.com/adi-g15/run"
license=('Unlicense')
depends=('gcc')
makedepends=('git')
provides=("run")
source=('git+https://github.com/adi-g15/run.git')
md5sums=('SKIP')

pkgver() {
	cd "$srcdir/run"

	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	cd "$srcdir/run"
	make
}

package() {
	cd "$srcdir/run"
	DESTDIR="$pkgdir/" make install
}
