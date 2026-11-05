# Maintainer: Simone Balducci <simone.balducci00@gmail.com>
pkgname=alpaka
pkgver=2.2.0
pkgrel=1
pkgdesc=""
arch=(any)
url="https://github.com/alpaka-group/alpaka"
license=('MPL-2.0')
depends=(boost)
makedepends=(cmake)
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
source=(https://github.com/alpaka-group/alpaka/archive/refs/tags/2.2.0.tar.gz)
sha256sums=('b38dc3f461da261a746956bd84ae85c62a9b3ef13c078c94bceb9783ae94d1f2')

build() {
    cd "$srcdir/CLUEstering-$pkgver"
    mkdir -p build
    cd build
    cmake .. -DCMAKE_INSTALL_PREFIX=/usr
    # No compilation needed; CMake will configure installation
}

package() {
    cd "$srcdir/alpaka-$pkgver/build"
    cmake --install . --prefix "$pkgdir/usr"
}
