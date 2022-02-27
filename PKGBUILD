# Maintainer: Changseo Jang <changseo.jang@korea.edu>
pkgname='pbkit'
pkgver='v0.0.22'
pkgrel=5
pkgdesc='Protobuf Dependency Manager'
arch=('x86_64')
url='https://github.com/pbkit/pbkit'
license=('MIT' 'APACHE')
depends=()
makedepends=('git' 'deno')
source=("pbkit::git://github.com/pbkit/pbkit.git#tag=${pkgver}")
sha256sums=('SKIP')

build() {
  cd ${pkgname}

  mkdir build
  deno compile --unstable -A --output build/pollapo ./cli/pollapo/entrypoint.ts
  deno compile --unstable -A --output build/pb ./cli/pb/entrypoint.ts

  ls -al
  ls -al build
}

package() {
  ls -al ${pkgname}/build

  install -dm755 ${pkgdir}/usr/bin
  mv ${pkgname}/build/pollapo ${pkgdir}/usr/bin/pollapo
  mv ${pkgname}/build/pb ${pkgdir}/usr/bin/pb
}
