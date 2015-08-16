#Maintainer : Vadim Ushakov <igeekless [at] gmail [dot] com>

pkgname=libsde-utils-x11-git
pkgver=201507291344
pkgrel=1
url="http://make-linux.org"
pkgdesc="SDE Utility Library"
arch=('i686' 'x86_64')
license=('GPL')
depends=('libsde-utils-git' 'libx11' 'sde-reverse-meta-git')
makedepends=('git' 'intltool' 'pkgconfig' 'cmake')
provides=('libsde-utils-x11' )
conflicts=('libsde-utils-x11')

source=('git+git://make-linux.org/sde/libsde-utils-x11.git')
md5sums=('SKIP')

_gitname="libsde-utils-x11"

pkgver() {
  date +%Y%m%d%H%M
}

build() {
    cd "${_gitname}"
    cmake -DCMAKE_INSTALL_PREFIX=/usr . && make
}

package () {
    cd "${_gitname}"
    make DESTDIR="$pkgdir/" install
}

