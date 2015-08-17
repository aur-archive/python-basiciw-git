# Maintainer: CJlano <cjlano+AUR.basiciw@free.fr>

pkgname=python-basiciw-git
_gitname=basiciw
pkgver=0.5.456e3f6
pkgrel=1
pkgdesc="Retrieve information such as ESSID or signal quality from wireless cards (Python module)"
arch=('i686' 'x86_64')
url="https://github.com/enkore/basiciw/"
license=('MIT')
depends=('python' 'wireless_tools')
makedepends=('git')
conflicts=basiciw-git
provides=basiciw-git
replaces=basiciw-git
source=('git://github.com/enkore/basiciw.git')
md5sums=('SKIP')

pkgver() {
  cd $_gitname
  echo "0.$(git rev-list --count HEAD).$(git describe --always )"
}

package() {
  cd "$srcdir"/$_gitname
  python setup.py install --root "$pkgdir"

  # Install README file
  install -Dm644 README "${pkgdir}/usr/share/${pkgname}/README"
}

# vim:set ts=2 sw=2 et:
