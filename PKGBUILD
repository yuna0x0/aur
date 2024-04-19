# Maintainer: Edison Lee <edisonlee@edisonlee55.com>
pkgname=cirno-catch-frog
pkgver=1.0.3
pkgrel=1
pkgdesc="Touhou fan game made with Godot. Let's help Cirno catch frogs!"
arch=('x86_64')
url="https://edisonlee55.itch.io/cirno-catch-frog"
license=('custom')
options=(!strip !debug)
source=("https://cdn.edisonlee55.com/projects/${pkgname}/releases/v${pkgver}/CirnoCatchFrog-Linux_${arch}-${pkgver}.zip")
sha256sums=('c2c51cd5dcd591a4f5dee6e80e9e480e09a19719a4e8202db79517d2092d4963')

package() {
	mkdir -p ${pkgdir}/usr/{share/$pkgname,bin}/
	cp -f "${srcdir}/CirnoCatchFrog-Linux_${arch}-${pkgver}/CirnoCatchFrog.${arch}" "${pkgdir}/usr/share/${pkgname}/"
	chmod 755 -R ${pkgdir}/usr/share/${pkgname}/*
	ln -sf "${pkgdir}/usr/share/${pkgname}/CirnoCatchFrog.${arch}" "${pkgdir}/usr/bin/${pkgname}"
}
