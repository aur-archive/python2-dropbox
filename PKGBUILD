# Maintainer: Tim Diels <tim@timdiels.be>
pkgname=python2-dropbox
pkgver=2.2.0
pkgrel=2
pkgdesc="Python SDK for Dropbox Core APIs"
url='https://www.dropbox.com/developers/core/sdk'
arch=('any')
license=('MIT')
depends=('python2' python2-urllib3)
makedepends=('python2-setuptools')
source=(https://pypi.python.org/packages/source/d/dropbox/dropbox-${pkgver}.zip)
md5sums=('8f9bc437c19b34670aff2526e30c855a')

build() {
  cd ${srcdir}/dropbox-${pkgver}
  python2 setup.py install --root=${pkgdir} -O1
  sed -i -e "s|#![ ]*/usr/bin/python$|#!/usr/bin/python2|" \
         -e "s|#![ ]*/usr/bin/env python$|#!/usr/bin/env python2|" \
    $(find $pkgdir -name '*.py')
}
