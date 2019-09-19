# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=treos-local-config
pkgver=1.0.2
pkgrel=1
pkgdesc="Track station and apply configuration to local system"
arch=('x86_64')
license=('GPL')
groups=()
depends=(
makedepends=('npm')

pkgver () {
  npm view ${pkgname}@latest version
}

package () {
  source "$HOME/.nvm/nvm.sh"
  nvm use 10.8.0
  local _npmdir="${pkgdir}/usr/lib/node_modules/"
  mkdir -p $_npmdir
  npm install -g --prefix "${pkgdir}/usr" ${pkgname}@${pkgver}
}
