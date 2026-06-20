# Maintainer: Wind_Blood <windblood@foxmail.com>

pkgname=touphinx
pkgver=1.0.0
pkgrel=1
pkgdesc="Dolphin with enhanced touchscreen behavior"
arch=('x86_64')
url="https://github.com/JPTV-21/Touphinx"
license=('GPL2')
depends=('dolphin' 'git' 'make' 'gcc' 'cmake' 'extra-cmake-modules' 'kcoreaddons' 'kio' 'kitemmodels')
source=("dolphin::git+https://invent.kde.org/system/dolphin.git"
        "touphinx.patch")
sha256sums=('SKIP'
            'SKIP')

prepare() {
  cd "$srcdir/dolphin"
  git apply "$srcdir/touphinx.patch"
}

build() {
  cd "$srcdir/dolphin"
  mkdir -p build && cd build
  cmake .. -DCMAKE_INSTALL_PREFIX=/usr
  make
}

package() {
  cd "$srcdir/dolphin/build"
  make DESTDIR="$pkgdir" install
}
