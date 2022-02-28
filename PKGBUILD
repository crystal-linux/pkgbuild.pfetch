# Crystal Maintainer: echo -n 'bWF0dEBnZXRjcnlzdC5hbA==' | base64 --decode
# AUR Maintainer: timescam <rex.ky.ng at gmail dot com>

_pkgname=pfetch
pkgname=pfetch
pkgver=69_0.6.0
pkgrel=1
pkgdesc="A pretty system information tool written in POSIX sh."
arch=(any)
url="https://github.com/dylanaraps/$_pkgname"
license=('MIT')
makedepends=('git')
provides=("$_pkgname")

source=("$_pkgname::git+https://github.com/dylanaraps/$_pkgname.git")
md5sums=('SKIP')

pkgver() {
            cd "$srcdir/$_pkgname"
            echo "r$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

package () {
            install -Dm755 "$srcdir/$_pkgname/pfetch" "$pkgdir/usr/bin/pfetch"
}
