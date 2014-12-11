# Maintainer: TuxSpirit<tuxspiritATarchlinuxDOTfr>

pkgname=slimconf
_pkgname=SLiMconf
pkgver=20120809
pkgrel=10
pkgdesc="Slim GUI Configure"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('git')
depends=('slim' 'pygtk')
url="https://github.com/corenominal/SLiMconf"
source=("git+git://github.com/corenominal/SLiMconf.git")
md5sums=('SKIP')

_gitname="slimconf"


prepare(){
  cd "${srcdir}/${_pkgname}"
  
  patch -uN slimconf ../../slimconf.patch 
}

package() {   
  cd "$srcdir"
  install -D -m755 $srcdir/$_pkgname/$pkgname "$pkgdir/usr/bin/$pkgname"
  install -D -m755 $srcdir/$_pkgname/$pkgname-ui.glade "$pkgdir/usr/share/$pkgname/glade/$pkgname-ui.glade"
  
}  
