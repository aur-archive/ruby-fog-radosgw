# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=fog-radosgw
pkgname=ruby-$_gemname
pkgver=0.0.3
pkgrel=1
pkgdesc='Fog backend for provisioning Ceph Radosgw.'
arch=(any)
url='https://github.com/fog/fog-radosgw'
license=(MIT)
depends=(ruby ruby-fog-json ruby-fog-xml ruby-fog-core)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('2560ce7684a8e5ead362254d08a105e80cf6b168')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.md" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.md"
}
