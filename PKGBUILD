pkgname="crowdstrike-falcon-sensor-bin"
pkgver="6.34.0_13108"
pkgrel=5
pkgdesc="CrowdStrike Falcon Sensor binaries"
arch=("x86_64")
url="https://www.crowdstrike.com/"
license=("custom")
depends=("glibc" "gcc-libs")
install="falcon-sensor-bin.install"
source=("local://Ub_falcon-sensor_${pkgver//_/-}_amd64.deb")
sha256sums=("3223aec2755adefe1228fb6ae2d6ac6b0d68aef79050b2ed27449c1280b7ed85")

package() {
        tar -xf data.tar.xz
        mkdir ${pkgdir}/usr/
	cp --no-dereference --preserve=mode,links,timestamps --recursive opt "${pkgdir}"
	cp --no-dereference --preserve=mode,links,timestamps --recursive lib "${pkgdir}/usr/lib"
}
