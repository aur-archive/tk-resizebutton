# Maintainer: Archie <xMickael@ifrance.com>

pkgname=tk-resizebutton
pkgver=0.01
pkgrel=2
pkgdesc="provides a resizeable button to be used in an HList column header."
depends=('tk')
arch=('i686')
license=('GPL')
source=(http://search.cpan.org/CPAN/authors/id/X/XP/XPIX/Tk-ResizeButton-$pkgver.tar.gz)
url="http://search.cpan.org/~xpix/Tk-ResizeButton/"
md5sums=('b1c782ec46e3bcb7e52fdd5909645ad2')

build() {
  cd $startdir/src/Tk-ResizeButton-$pkgver
  perl Makefile.PL
  make || return 1
  make DESTDIR=$startdir/pkg/ install
  /usr/bin/find $startdir/pkg -name '.packlist' -exec rm '{}' \;
  /usr/bin/find $startdir/pkg -name 'perllocal.pod' -exec rm '{}' \;
}
