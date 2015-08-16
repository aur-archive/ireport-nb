# Maintainer: Igor Dejanovic <igor DOT dejanovic AT gmail DOT com>
# Contributor: Igor Dejanovic <igor DOT dejanovic AT gmail DOT com>
# Based on netbeans PKGBUILD

pkgname=ireport-nb
_pkgname=iReport
pkgver=5.5.0
pkgrel=1
pkgdesc="A visual report builder for JasperReports based on NetBeans RCP"
license="AGPL"
source=(http://switch.dl.sourceforge.net/project/ireport/iReport/$_pkgname-$pkgver/$_pkgname-$pkgver.tar.gz $pkgname.desktop)
url="http://sourceforge.net/projects/ireport/"
depends=("java-runtime")
arch=('i686' 'x86_64')

package() {

  cd $srcdir
  mkdir -p $pkgdir/usr/share/$pkgname

  rm $srcdir/$_pkgname-$pkgver/bin/*.exe

  cp -r $srcdir/$_pkgname-$pkgver/* $pkgdir/usr/share/$pkgname/
  
  install -D -m644 $srcdir/$_pkgname-$pkgver/LICENSE_ireport.txt $pkgdir/usr/share/licenses/$pkgname/LICENSE
  install -D -m644 $srcdir/$pkgname.desktop $pkgdir/usr/share/applications/$pkgname.desktop

  mkdir -p $pkgdir/usr/bin
  ln -s /usr/share/$pkgname/bin/ireport $pkgdir/usr/bin/

}

md5sums=('670d1454979e3ded6c2fe298cd35f76c'
         '7d9e041db04feba100c036d5e70edb89')
