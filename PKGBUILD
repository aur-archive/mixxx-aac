# Maintainer: David J. Haines <djhaines at gmx dot com>
# Contributor: Lukas Fleischer <archlinux at cryptocrack dot de>
# Contributor: Ali H. Caliskan <ali.h.caliskan AT gmail DOT com>
# Contributor: Ryan Coyner <rcoyner@gmail.com>
# Contributor: Stefan Husmann <stefan-husmann@t-online.de>

pkgname=mixxx-aac
pkgver=1.11.0
pkgrel=1
pkgdesc="Free, open source software for digital DJ'ing with AAC support enabled."
arch=('i686' 'x86_64')
url='http://www.mixxx.org'
license=('GPL')
depends=('fftw' 'libid3tag' 'libmad' 'libogg' 'libshout' 'libsndfile' 'portaudio' 'portmidi' 'taglib' 'qtwebkit' 'vamp-plugin-sdk' 'libusbx' 'protobuf' 'faad2' 'libmp4v2')
makedepends=('mesa' 'scons' 'libshout' 'glu')
provides=('mixxx')
conflicts=('mixxx')
source=("http://downloads.mixxx.org/mixxx-${pkgver}/mixxx-${pkgver}-src.tar.gz")
md5sums=('89ee8ba60824919d8dd1194287bda259')

build() {
    cd "${srcdir}/mixxx-${pkgver}"
    scons qtdir=/usr/lib/qt4 prefix=/usr faad=1
}

package() {
    cd "${srcdir}/mixxx-${pkgver}"
    scons qtdir=/usr/lib/qt4 prefix=/usr faad=1 install_root="${pkgdir}/usr" install
}
