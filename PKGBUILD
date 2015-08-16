# Maintainer: m4xm4n <max@maxfierke.com>
pkgname=gtk-theme-bleufear-git
pkgver=20141026
pkgrel=1
pkgdesc="Official AUR build for a dark theme with a dash of electric blue."
url="https://github.com/maxfierke/BleuFear"
license=('GPL3')
arch=('any')
depends=('gtk-engines' 'gtk-engine-murrine')
# Added so as not to conflict with any future "stable" (non-git) versions.
provides=('gtk-theme-bleufear')
makedepends=('git')

_gitroot="https://github.com/maxfierke/BleuFear.git"
_gitname="BleuFear"

build() {
  cd $srcdir
  msg "Grabbing the latest version from Github..."
  if [[ -d $srcdir/$_gitname ]] ; then
    cd ${_gitname}
    git pull origin
    msg "Working directory updated!"
  else
    git clone $_gitroot $_gitname
  fi
  msg "Git clone completed."
}

package() {
    cd $srcdir
    mkdir -p $pkgdir/usr/share/themes
    mv BleuFear $pkgdir/usr/share/themes
}

