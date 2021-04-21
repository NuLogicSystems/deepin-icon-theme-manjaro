# $Id$
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>
# Contributor: Felix Yan <felixonmars@archlinux.org>
# Contributor: Josip Ponjavic <josipponjavic at gmail dot com>
# Contributor: Xu Fasheng <fasheng.xu[AT]gmail.com>

pkgname=deepin-icon-theme-manjaro
_pkgname=deepin-icon-theme
pkgver=2021.03.12
pkgrel=1
pkgdesc="Deepin Icons themed for Manjaro"
arch=('any')
url="https://github.com/linuxdeepin/deepin-icon-theme"
license=('GPL3')
depends=('papirus-icon-theme')
provides=('deepin-cursor-theme' 'deepin-icon-theme')
conflicts=('deepin-cursor-theme' 'deepin-icon-theme')
groups=('deepin-manjaro')
source=("$_pkgname-$pkgver.tar.gz::https://github.com/linuxdeepin/deepin-icon-theme/archive/$pkgver.tar.gz"
        $_pkgname-fix-installation-2021.03.12.patch::https://github.com/linuxdeepin/deepin-icon-theme/pull/23.patch
        deepin-launcher.svg)

sha512sums=('cc5c22225ccef5d67e786ca2154f7473d8ff1823c42adfe722a45d4e46e3d3493f65213210692e95e5b229b295c49ee54041e7e292ee0443ac5e406ba61490b2'
            '5c2ed40893093ec161776a86093e2589bff95b2a8150d18e266a86a439c854dec9ec95304a0d8b684be0cc22aece35a0d1ee7a05484f03b63681a23000e26d67'
            'c03511e77d7dd2ec0e9054f39c9fef4e086b685618d746e447be2bb48e4a34b41b44acc104bf5fedd919e8a2bcd123d7ea27426c2d315cfa27d8f24b14c2fc0e')

prepare() {
  patch -d $_pkgname-$pkgver -p1 < $_pkgname-fix-installation-2021.03.12.patch
  sed -i 's/deepin/bloom/g' $_pkgname-$pkgver/tools/hicolor.links

  # Broken filenames are not dealt since reported in June 2020. Let's clean them up ourselves.
  find $_pkgname-$pkgver -name "* 2.svg" -delete

}

build() {
  cd $_pkgname-$pkgver
  make hicolor-links
}

package() {
  cd $_pkgname-$pkgver
  make DESTDIR="$pkgdir" install

  cp -a ./Sea ./usr/share/icons/hicolor "$pkgdir"/usr/share/icons/

  #replace the bloom deepin-launchers with a manjaro themed deepin-launcher
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/16/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/24/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/32/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/48/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/64/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/96/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/128/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/256/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom/places/512/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic/places/22/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic/places/24/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic/places/32/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic/places/48/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic/places/64/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic/places/96/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic/places/128/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic/places/256/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic-dark/places/22/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic-dark/places/24/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic-dark/places/32/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic-dark/places/48/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic-dark/places/64/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic-dark/places/96/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic-dark/places/128/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-classic-dark/places/256/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/16/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/24/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/32/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/48/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/64/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/96/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/128/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/256/deepin-launcher.svg
  cp -f ../deepin-launcher.svg "$pkgdir"/usr/share/icons/bloom-dark/places/512/deepin-launcher.svg
}
