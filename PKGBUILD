# Maintainer: Amadeus Folego aka badosu <amadeusfolego at gmail dot com>
pkgname=nvdiablperm
pkgver=0.1
pkgrel=1
pkgdesc="Give nvidia keyboard backlight permission for all users"
arch=(any)
url="https://github.com/badosu/nvidiablperm"
license=('GPL')
depends=('bash')
source=(
  https://github.com/badosu/nvidiablperm/raw/master/nvidiablperm
  https://github.com/badosu/nvidiablperm/raw/master/nvidiablperm.service)
sha256sums=(
  "9a8ceb6bb79ab21ec83397db7a42521a402e4f7b5bf67616a4ee1171d75b4e5a"
  "6e3afbce95f41d5379a15aab2a82bd1eb8356d371feec8bfae90ce11ae74b532")

package() {
  cd $srcdir
  install -Dm755 nvidiablperm $pkgdir/usr/bin/nvidiablperm
  install -Dm644 nvidiablperm.service "${pkgdir}$(pkg-config systemd --variable=systemdsystemunitdir)/nvidiablperm.service"
}

# vim: set ts=2 sw=2 et:
