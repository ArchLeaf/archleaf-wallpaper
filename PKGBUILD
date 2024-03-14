_pkgname=archleaf-wallpaper
pkgname=archleaf-wallpaper
pkgver=1.0.0
pkgrel=1
pkgdesc='All of archleaf wallpaper'
arch=(any)
url='https://gitea.com/KnoyanMitsu'
_url="https://gitea.com/KnoyanMitsu"
license=('CC-BY-SA')
source=("$_url/$pkgname/archive/refs/tags/v$pkgver.tar.gz")

sha256sums=('1dc826ec54d8751bae89cb9604327a150d62b6d73d68bb041ce1b7e788d6f2d3')

package() {

	cd "$srcdir/$pkgname-$pkgver/$_pkgname"

	# Creating needed directories
	install -dm755 "${pkgdir}/usr/share/backgrounds/$_pkgname/"

	# Wallpapers
	local wallpaper
	for wallpaper in *; do
		install -m755 "$srcdir/$pkgname-$pkgver/$_pkgname/${wallpaper}" "$pkgdir/usr/share/backgrounds/$_pkgname/${wallpaper}"
	done
}
