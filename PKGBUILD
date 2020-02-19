# Maintainer: Caleb Maclennan <caleb@alerque.com>
# PKGBUILD generated by pipman
# Python package author: Kolen Cheung <christian.kolen@gmail.com>

_name=pantable
pkgname=python-$_name
pkgver=0.12.2
pkgrel=3
pkgdesc='CSV Tables in Markdown: Pandoc Filter for CSV Tables'
arch=('any')
url="https://github.com/ickc/$_name"
license=('GPL3')
_pydeps=('click'
         'future'
         'pandoc-include'
         'panflute'
         'yaml'
         'shutilwhich')
depends=('python'  "${_pydeps[@]/#/python-}")
makedepends=('python-setuptools')
source=("https://github.com/ickc/$_name/archive/v$pkgver.tar.gz")
sha256sums=('c71e9a8cba7dac8420e4cc089ad518a62a0f571bf85f406f87b553cf411d6ddd')

build() {
	cd "$_name-$pkgver"
	python setup.py build
}

package() {
    cd "$_name-$pkgver"
    python setup.py install --root="$pkgdir" --optimize=1 --skip-build
}
