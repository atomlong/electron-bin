# Maintainer: Yurii Kolesnykov <root@yurikoles.com>

# Based on extra/electron by
# Caleb Maclennan <caleb@alerque.com>
# Bruno Pagani <archange@archlinux.org>

pkgver=31
pkgrel=1
_pkgname=electron
pkgname="${_pkgname}-bin"
pkgdesc='Meta package providing the latest available stable Electron build'
pkgdesc+=' — binary'
arch=(any)
url='https://electronjs.org'
license=(MIT)
provides=("${_pkgname}=${pkgver}")
conflicts=("${_pkgname}")

package() {
	depends=("electron${pkgver}-bin")
	mkdir -p "${pkgdir}/usr/bin" "${pkgdir}/usr/lib"

	local _electron_major="electron${pkgver}"
	ln -sf "${_electron_major}" "${pkgdir}/usr/bin/${pkgname}"
	ln -sf "${_electron_major}" "${pkgdir}/usr/lib/${pkgname}"
}
