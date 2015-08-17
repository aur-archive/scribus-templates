# Maintainer: Limao Luo <luolimao+AUR@gmail.com>

pkgname=scribus-templates
pkgver=1.3.8
pkgrel=1
pkgdesc="An extended package of document templates for Scribus."
arch=(i686 x86_64)
url=http://sourceforge.net/projects/scribus/files/extras/templates/
license=(custom)
depends=(scribus)
source=(http://downloads.sourceforge.net/project/scribus/extras/templates/presentation_templates-0.1.zip)
sha256sums=('2785336eb5bd587b66f56b5fcf35d9a32704631965987645ebd66e0ffe882406')
sha512sums=('23cf1da77c5f8b38db8dcf9225f32a1e5ea727f4f8ce4f3970b64c6f9aefb48713f944dc03a26b66c4f0dd14b116a8e3654f69895270eda1838110f242940f9a')

package() {
    cd "$srcdir"/presentation_templates/
    for i in *.png *.sla.gz template.xml; do
        install -Dm644 $i "$pkgdir"/usr/share/scribus/templates/presentation_templates/$i
    done
    install -Dm644 license.pdf "$pkgdir"/usr/share/licenses/$pkgname/LICENSE.pdf
}
