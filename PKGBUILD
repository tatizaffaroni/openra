pkgname=openra
pkgver=20160508
pkgrel=1
pkgdesc='A multiplayer re-envisioning of early RTS games by Westwood Studios.'
arch=('x86_64')
url='http://www.openra.net/'
license=('GPL3')
depends=("openal" "mono" "freetype2" "glibc" "alsa-lib" "libgl" "xdg-utils" "qarma" "sdl2" "lua")
source=("https://github.com/OpenRA/OpenRA/releases/download/release-${pkgver}/${pkgname}_release.${pkgver}_all.deb")
md5sums=('7eb75c2e826362febcc7be7e05066aab')

package() {
    tar -xvf data.tar.gz -C $pkgdir
    rm -r $pkgdir/usr/share/doc
    ln -s /usr/lib/liblua.so.5.1 $pkgdir/usr/lib/liblua5.1.so.0
    install -Dm644 $pkgdir/usr/share/icons/hicolor/scalable/apps/openra.svg $pkgdir/usr/share/pixmaps/$pkgname.svg
    rm -r $pkgdir/usr/share/icons
    cd $pkgdir/usr && mv games bin
    }

