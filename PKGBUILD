pkgname=exz
pkgver=1.0.0
pkgrel=1
pkgdesc="Executable XZipped Archive"
arch=('any')
url="https://github.com/TheOddCell/exz"
license=('MIT')
depends=('python3' 'tar' 'xz' 'coreutils' 'bash')
makedepends=()
source=('exz-maker' 'appimage-to-exz')
sha256sums=('SKIP' 'SKIP')

package() { install -Dm755 exz-maker "$pkgdir/usr/bin/exz-maker";install -Dm755 appimage-to-exz "$pkgdir/usr/bin/appimage-to-exz"; }
