# Maintainer: fubarhouse
pkgname=backport-iwlwifi
pkgver=8725102f41cd5e21dc0251a30b0f48b5f3d0d4a5
pkgrel=1
pkgdesc="Backported support for iwlwifi sourced from the Ubuntu community"
arch=('x86_64')
url="https://github.com/fubarhouse/backport-iwlwifi.pkgbuild"
license=('MIT')
depends=(linux-firmware-iwlwifi-git)
makedepends=(git make sudo)
source=(git://git.kernel.org/pub/scm/linux/kernel/git/iwlwifi/backport-iwlwifi.git)
sha512sums=('SKIP')

pkgver() {
  cd "$pkgname"
  git rev-parse HEAD
}

build(){
  cd "$pkgname"
  echo "#include \"reg.h\"" > net/wireless/shipped-certs.c
  echo "const u8 shipped_regdb_certs[] = {};" >> net/wireless/shipped-certs.c
  echo "unsigned int shipped_regdb_certs_len = sizeof(shipped_regdb_certs);" >> net/wireless/shipped-certs.c
  sudo make install
}

package() {
  echo "Do not forget to reboot!";
}