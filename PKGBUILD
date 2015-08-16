#Contributor: box0 

pkgname=kontainer
_realname=kontainer
pkgver=0.5
pkgrel=1
pkgdesc='A rudimentary nested Windowmanager, tiling clients vertically, horizontally or a row or column oriented grid.'
arch=('i686' 'x86_64')
url='http://kde-look.org/content/show.php/Kontainer?content=157471'
license=('GPL')
conflicts=()
depends=('kdebase-workspace')
makedepends=('cmake' 'automoc4')
source=(http://kde-look.org/CONTENT/content-files/157471-Kontainer.txz)
md5sums=('a9cedbc823f3f0c4d8148086f38bd927')


build() {
    mkdir build
    cd build
    cmake ../Kontainer \
            -DCMAKE_BUILD_TYPE=Release \
            -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` \
            -DQT_QMAKE_EXECUTABLE=qmake-qt4
    make
}
package() {
  cd build
  make DESTDIR=$pkgdir install
} 
