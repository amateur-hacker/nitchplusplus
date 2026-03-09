# Maintainer: clamsfeel2 <clamsfeel@proton.me>
pkgname="nitch++-git"
pkgdesc="System information fetch tool written in C++"
pkgver=0.1.0
pkgrel=1
arch=('x86_64')
license=('MIT')
url="https://github.com/clamsfeel2/nitchplusplus"
source=("git+https://github.com/clamsfeel2/nitchplusplus.git#commit=HEAD")
makedepends=('gcc' 'cmake' 'ninja')
sha256sums=('SKIP') # Skip since using latest commit
options=('!debug')
# validpgpkeys=(4FE361904964CAC3E1CE241D57A36E69AE3A6842) # Not sure if tihs is correct GPG implentation, so commenting for now.

build() {
  cmake -B build -S nitchplusplus -GNinja \
    -DCMAKE_BUILD_TYPE=Release
  ninja -C build
}

package() {
  install -Dm755 build/nitch++ "$pkgdir/usr/bin/nitch++"
}
