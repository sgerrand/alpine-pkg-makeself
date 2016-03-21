# Contributor: Sasha Gerrand <alpine-pkg-makeself@sgerrand.com>
# Maintainer: Sasha Gerrand <alpine-pkg-makeself@sgerrand.com>
pkgname=makeself
pkgver=2.2.0
pkgrel=0
pkgdesc="Make self-extractable archives on Unix"
url="http://www.megastep.org/makeself"
arch="noarch"
license="GPL"
depends=""
makedepends="busybox"
install=""
subpackages="$pkgname-doc"
source="http://cdn.megastep.org/$pkgname/$pkgname-$pkgver.run"

_builddir="$srcdir/$pkgname-$pkgver"

build() {
  cd "$_builddir"
  sh $pkgname-$pkgver.run
}

package() {
  cd "$_builddir"
  install -Dm755 $pkgname.sh "$pkgdir"/usr/bin/$pkgname
  install -Dm644 COPYING "$pkgdir"/usr/share/license/$pkgname/COPYING
}

doc() {
  cd "$_builddir"
  mkdir -p "$subpkgdir"/usr/share/man/man1 || return 1
  gzip -9 $pkgname.1
  mv $pkgname.1.gz "$subpkgdir"/usr/share/man/man1/

  for _doc in README.md $pkgname-header.sh
  do
    install -Dm644 $_builddir/$_doc "$subpkgdir"/usr/share/doc/$pkgname/$_doc || return 1
  done
}

md5sums="a2ecb4e27dc757da37fbaca3cb176854  makeself-2.2.0.run"
sha256ums="3651adc6bde627e93911c28e696f7fd6b2849e0b2677ca368f3b8be97703922a  makeself-2.2.0.run"
sha512ums="4a5fa909f7c26041b4df3564ddc58cb401832bac13c63c50db989dc705e8d4dd1cdf398d64fdd14fca59694af0df86349457565479b8aa5038e5d2b14658545a  makeself-2.2.0.run"
