# Contributor: Tomas A. Schertel <tschertel@gmail.com>

pkgname=crebs
pkgver=0.9.8.5
pkgrel=2
pkgdesc="a Python/GTK application used to create and set desktop wallpaper slideshows for GNOME"
arch=(any)
url="http://www.obfuscatepenguin.net/"
source=(http://www.obfuscatepenguin.net/source/crebs.tar.gz
	arch-python-stuff.patch)
license=('GPL')
md5sums=('c5c7edac5aa557ce2727b0e8b651b939'
	 '2a93baea552f8c35d7b78e31abfad7f1')
depends=('python2' 'python2-notify' 'python2-gconf')
options=(!emptydirs)
install=$pkgname.install
build() {
 patch -Np1 -i "${srcdir}/arch-python-stuff.patch" || return 1
 cd $srcdir/crebs-$pkgver
 mkdir $pkgdir/usr
 ./setup.sh -p "$pkgdir"/usr || return 1

 }
