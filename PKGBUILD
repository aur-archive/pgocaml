# Contributor: spider-mario <spidermario@free.fr>
pkgname=pgocaml
pkgver=1.5
pkgrel=1
pkgdesc="Interface to PostgreSQL databases for OCaml applications"
arch=('i686' 'x86_64')
url="http://pgocaml.forge.ocamlcore.org/"
license=('custom:LGPL')
depends=('ocaml' 'ocaml-extlib' 'ocaml-calendar' 'ocaml-csv' 'ocaml-pcre')
makedepends=('ocaml-findlib')
source=(http://forge.ocamlcore.org/frs/download.php/850/$pkgname-$pkgname.tgz)
md5sums=('2b955d53b8823b12caeb19c5e1ffdb7c')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  echo "DESTDIR := \"$pkgdir/\"" >> Makefile.config
  make depend
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make install
  install --directory "$pkgdir/usr/share/licenses/$pkgname/"
  install COPYING.LIB "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# vim:set ts=2 sw=2 et:
