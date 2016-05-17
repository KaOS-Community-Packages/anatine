pkgname=anatine
pkgver=0.3.0
pkgrel=1
pkgdesc="An open source twitter client based on chromium"
arch=('x86_64')
url="https://github.com/sindresorhus/anatine"
license=('MIT')  
source=("https://github.com/sindresorhus/anatine/releases/download/${pkgver}/Anatine-linux-${pkgver}.zip" "anatine.png" "anatine.desktop")
depends=("gtk2" "gconf" "nss" "libnotify" "alsa-lib" "libxtst")
md5sums=('37c6238ab8f31274282e353c050ee350'
         '9a820cd4774a853aa8b23951220e0d89'
         '7465785fc2e03d981d2978843cdc6334')

package() {
   install -dm755 $pkgdir/usr/share/anatine 
   cp -r $srcdir/* $pkgdir/usr/share/anatine
   rm $pkgdir/usr/share/anatine/Anatine-linux-${pkgver}.zip
   rm $pkgdir/usr/share/anatine/anatine.desktop
   rm $pkgdir/usr/share/anatine/anatine.png
   
   install -Dm644 $srcdir/anatine.desktop $pkgdir/usr/share/applications/anatine.desktop
   
   install -Dm644 $srcdir/anatine.png $pkgdir/usr/share/pixmaps/anatine.png
   
   install -dm755 $pkgdir/usr/bin
   ln -s  /usr/share/anatine/Anatine $pkgdir/usr/bin/Anatine 
    }   




