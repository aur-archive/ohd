pkgname=ohd
pkgver=20120303
pkgrel=3
pkgdesc="simple hex dump tool."
url="http://www.club.kyutech.ac.jp/~opamp/projects/old/ohd/index.html"
arch=('i686' 'x86_64')
license=('BSD')
source=("http://www.club.kyutech.ac.jp/~opamp/projects/old/ohd/ohd.tar.bz2")
makedepends=('cmake')

build() {
	cd ${srcdir}/$pkgname
	mkdir build &&cd build

	cmake -DCMAKE_INSTALL_PREFIX=/usr ../
	make
}

package() {
	cd $srcdir/$pkgname/build
	make DESTDIR="$pkgdir" install
}
md5sums=("7a8d58afdf9d8ddd16a4cc182a68b2ac")
