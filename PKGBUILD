# Contributor: Ilya Mezhirov <mezhirov@iupr.com>

pkgname=vlfeat-docs
pkgver=0.9.16
pkgrel=2
pkgdesc="Documentation for vlfeat, a library of computer vision algorithms covering feature extraction, data clustering and image segmentation."
arch=('any')
url="http://www.vlfeat.org"
license=('BSD')
md5sums=('c2c03ed46e0fe0ed5c24b922dba76494')

makedepends=('transfig' 'doxygen' 'imagemagick' 'texlive-bin' 'texlive-core' 'python2' 'groff' 'tidyhtml' 'inkscape' 'sed')
source=("$url/download/vlfeat-$pkgver.tar.gz")

build() {
    cd "$srcdir/vlfeat-$pkgver"
    mkdir -p doc/mdoc.build/helpsearch
    PYTHON=python2 make doc
    rmdir doc/mdoc/helpsearch

    mkdir -p "$pkgdir/usr/share/doc/vlfeat"
    mv doc/* "$pkgdir/usr/share/doc/vlfeat"
}

