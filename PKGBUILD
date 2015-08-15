# Maintainer: Maximilien Noal (noal dot maximilien at gmail dot com) [AUR: xcomcmdr]

pkgname=elzaudm-git
_gitname=touhy
_pkgprog=elzaudm
pkgver=58.7d9420c
pkgrel=1
pkgdesc="Elzen's ALSA mixer"
arch='any'
license='GPL3'
url='http://fadrienn.irlnc.org/touhy/'
groups='touhy'
depends=('touhy-git' 'pygtk' 'python2-pyalsaaudio')
makedepends='git'
md5sums=('SKIP'
  '3057bd15c46e0658fca346d96559d45f')
source=('git://fadrienn.irlnc.org/touhy' 'elzaudm.desktop')

pkgver() {
  cd ${srcdir}/${_gitname}
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd ${srcdir}/${_gitname}
  mkdir -p ${pkgdir}/usr/bin
  install ${_pkgprog} ${pkgdir}/usr/bin
  install -Dm 644 ${srcdir}/${_pkgprog}.desktop \
    ${pkgdir}/usr/share/applications/${_pkgprog}.desktop
}
