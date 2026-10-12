# Maintainer: bhaki18 <https://github.com/bhaki18>
pkgname=ani-cli-it-git
pkgver=4.16.0
pkgrel=1
pkgdesc="CLI per guardare anime in streaming e scaricarli (Italian fork di ani-cli da AnimeWorld con resume automatico)"
arch=('any')
url="https://github.com/bhaki18/ani-cli-it"
license=('GPL3')
depends=('curl' 'sed' 'grep' 'fzf')
optdepends=(
    'mpv: lettore multimediale predefinito consigliato (supporta anche ani-skip)'
    'aria2: necessario per scaricare gli episodi con la flag -d'
    'vlc: player alternativo'
    'rofi: menu interattivo alternativo'
    'dmenu: menu interattivo alternativo'
)
provides=('ani-cli-it')
conflicts=('ani-cli-it')
source=("$pkgname::git+https://github.com/bhaki18/ani-cli-it.git")
sha256sums=('SKIP')

package() {
    cd "$srcdir/$pkgname"
    install -Dm755 "./ani-cli" "$pkgdir/usr/bin/ani-cli-it"
    install -Dm644 "./ani-cli.1" "$pkgdir/usr/share/man/man1/ani-cli-it.1"
}
