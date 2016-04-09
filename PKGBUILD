pkgname=pulseaudio-equalizer
pkgver=2.7.0.2
pkgrel=1
pkgdesc="Equalizer interface for the LADSPA sound processing of PulseAudio"
arch=('x86_64')
url="http://www.webupd8.org/2013/10/system-wide-pulseaudio-equalizer.html"
license=('GPL3')
depends=('pygtk' 'pulseaudio' 'bc' 'swh-plugins' )
source=(http://ppa.launchpad.net/nilarimogard/webupd8/ubuntu/pool/main/p/${pkgname}/${pkgname}_${pkgver}.orig.tar.gz $pkgname.sh $pkgname.py)
md5sums=('c3c886a6017cb16408d47d0f5cd8549b'
         '6922523dabba2d34c032dcc58ecab95b'
         '161c570448ce3d339138ae5d26b422d6')
package() {
  sed -i 's|gnome-volume-control|multimedia-volume-control|g' $srcdir/$pkgname/usr/share/applications/$pkgname.desktop
  cp -rfp $srcdir/$pkgname/usr $pkgdir
  install $srcdir/$pkgname.sh $pkgdir/usr/bin/$pkgname
  install  $srcdir/$pkgname.py $pkgdir/usr/share/$pkgname/
}
