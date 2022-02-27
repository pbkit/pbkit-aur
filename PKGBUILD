# Maintainer: Changseo Jang <changseo.jang@korea.edu>
pkgname='pbkit'
pkgver='v0.0.22'
pkgrel=5
pkgdesc='Protobuf Dependency Manager'
arch=('x86_64')
url='https://github.com/pbkit/pbkit'
license=('MIT' 'APACHE')
depends=('gcc-libs')
makedepends=('git' 'deno')
source=("pbkit::git://github.com/pbkit/pbkit.git#tag=${pkgver}")
sha256sums=('SKIP')

# build() {
#   cd ${pkgname}
#
#   deno --version
#
#   deno compile --unstable -A --output pollapo ./cli/pollapo/entrypoint.ts
#   deno compile --unstable -A --output pb ./cli/pb/entrypoint.ts
# }

package() {
  cd ${pkgname}

  deno compile --unstable -A --output pollapo ./cli/pollapo/entrypoint.ts
  deno compile --unstable -A --output pb ./cli/pb/entrypoint.ts

  ls -l pollapo

  mkdir -p ${pkgdir}/usr/bin
  mv pollapo ${pkgdir}/usr/bin/pollapo

  ls -l ${pkgdir}/usr/bin/pollapo
}
