#Maintainer: Gergely Imreh <imrehg@gmail.com>>
#Conributor: twa022 <twa022 at gmail dot com>

pkgname=fusepy
pkgdesc="Python module that provides a simple interface to FUSE"
pkgver=20120601
pkgrel=1
arch=('any')
url="https://github.com/terencehonles/fusepy"
license=('ISC')
depends=('python2')
makedepends=('git')

_gitroot="git://github.com/terencehonles/fusepy.git"
_gitname="fusepy"


build() {
  cd "${srcdir}"
  msg "Connecting to GIT server...."

  if [ -d $_gitname ] ; then
    cd ${_gitname} && git pull origin
    msg "The local files are updated."
  else
    git clone ${_gitroot}
    cd ${_gitname}
  fi

  msg "GIT checkout done or server timeout"

  install -D -m755 fuse.py ${pkgdir}/usr/lib/python2.7/site-packages/fuse.py
} 
