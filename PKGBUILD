# Maintainer: Andreas B. Wagner <AndreasBWagner@pointfree.net>
# Contributor: Brendan Long <korin43@gmail.com>

pkgname=blast
pkgver=2.2.26
pkgrel=1
pkgdesc="Basic Local Alignment Search Tool: finds regions of similarity between biological sequences"
arch=('i686' 'x86_64')
url="http://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastHome"
license=('custom')
makedepends=()
options=()

_arch=$CARCH
[ $CARCH == i686 ] && _arch="ia32"
[ $CARCH == x86_64 ] && _arch="x64"
source=(ftp://ftp.ncbi.nlm.nih.gov/blast/executables/release/LATEST/blast-$pkgver-$_arch-linux.tar.gz)
[ $CARCH == i686 ] && md5sums=('875be33b3b4a7f3a3612843bed80545f')

[ $CARCH == x86_64 ] && md5sums=('809798a912f4fb37f62406201456df67')

package() {
	mkdir -p $pkgdir/usr/share/doc/blast/
	mkdir -p $pkgdir/usr/share/blast/
	mkdir -p $pkgdir/usr
	cp -r $srcdir/blast-$pkgver/bin $pkgdir/usr
	cp -r $srcdir/blast-$pkgver/doc/* $pkgdir/usr/share/doc/blast
	cp -r $srcdir/blast-$pkgver/data/* $pkgdir/usr/share/blast
}
# vim:set ts=2 sw=2 et:
