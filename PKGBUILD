#Contributor: Jake VanderKolk <jakevanderkolk@gmail.com>
#Contributor: Mihai Coman <mihai@m1x.ro>
#Maintainer: Brian Bidulock <bidulock@openss7.org>

pkgname=fbxkb
pkgver=1.0.0
pkgrel=1
pkgdesc="Keyboard indicator and switcher"
arch=('i686' 'x86_64')
url="http://fbxkb.sourceforge.net/"
makedepends=('git')
depends=('gtk2' 'libxmu')
depends_x86_64=('gdk-pixbuf-xlib')
license=('GPL')
source=("git+https://github.com/aanatoly/fbxkb.git#tag=${pkgver}")
md5sums=(SKIP)


build() {
  cd "$pkgname"
  ./configure --prefix=/usr
  make LDFLAGS="-Wl,-O1,--sort-common,-z,relro,-z,now"
}

package() {
  cd "$pkgname"
  make PREFIX="${pkgdir}/usr" install
}


