# Maintainer: Edison Lee <edisonlee@edisonlee55.com>
pkgname=cirno-catch-frog
pkgver=1.0.3
pkgrel=3
pkgdesc="Touhou fan game made with Godot. Let's help Cirno catch frogs!"
arch=('x86_64')
url="https://edisonlee55.itch.io/cirno-catch-frog"
license=('custom')
makedepends=('gendesk')
options=(!strip !debug)
source=("https://cdn.edisonlee55.com/projects/${pkgname}/releases/v${pkgver}/CirnoCatchFrog-Linux_${arch}-${pkgver}.zip"
	"https://cdn.edisonlee55.com/projects/${pkgname}/releases/v${pkgver}/${pkgname}_icon.png")
sha256sums=('c2c51cd5dcd591a4f5dee6e80e9e480e09a19719a4e8202db79517d2092d4963'
	'1f8ffa3dee9b46a9115ae90efd9cc12b5d66ec6bf3049c4e9ff010f1dd711c82')

prepare() {
	gendesk -n --pkgname "${pkgname}" --pkgdesc "${pkgdesc}" --name "Cirno Catch Frog" --categories "Game"
}

package() {
	install -D -t "${pkgdir}/usr/share/${pkgname}/" CirnoCatchFrog-Linux_${arch}-${pkgver}/*
	install -d "${pkgdir}/usr/bin/"
	ln -sf "../share/${pkgname}/CirnoCatchFrog.${arch}" "${pkgdir}/usr/bin/${pkgname}"

	install -Dm644 "${pkgname}.desktop" "${pkgdir}/usr/share/applications/${pkgname}.desktop"
	install -Dm644 "${pkgname}_icon.png" "${pkgdir}/usr/share/pixmaps/${pkgname}.png"
}
