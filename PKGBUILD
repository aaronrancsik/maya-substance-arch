_mayaver=2022

pkgname=maya-substance
pkgver=2.1.9
pkgrel=1
pkgdesc='Autodesk Maya Substance Plugin'
arch=('x86_64')
url='https://www.substance3d.com/ecosystem-plug-ins/substance-in-maya'
license=('custom')
depends=('maya>=2022.0' 'maya<2023.0')

DLAGENTS+=('manual::/usr/bin/echo \ \ Note: Please download the package manually from the official website')
source=("manual://SubstanceInMaya-$pkgver-$_mayaver-Linux.rpm")
sha256sums=('025dd73d895bb721f73847bbd88ed2f28ce3a653223d609210ebab4a4d9cf375')

options=(!strip)

prepare() {
    echo "+ PLATFORM:linux substance2 $pkgver /usr/autodesk/maya$_mayaver/plug-ins/substance2" > opt/Allegorithmic/Substance_in_Maya/$_mayaver/substance2.mod
    echo 'PATH+:=lib' >> opt/Allegorithmic/Substance_in_Maya/$_mayaver/substance2.mod
}

package() {
    mkdir -p $pkgdir/usr/autodesk/maya$_mayaver/{modules,plug-ins/substance2}

    mv opt/Allegorithmic/Substance_in_Maya/$_mayaver/substance2.mod $pkgdir/usr/autodesk/maya$_mayaver/modules/
    mv opt/Allegorithmic/Substance_in_Maya/$_mayaver/* $pkgdir/usr/autodesk/maya$_mayaver/plug-ins/substance2/
}
