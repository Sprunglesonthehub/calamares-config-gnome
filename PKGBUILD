pkgname=calamares-config-gnome
pkgver=3.3.9
pkgrel=2
pkgdesc="GNOME Calamares Config"
arch=('any')
url="https://github.com/Sprunglesonthehub/calamares-config-gnome"
license=('GPL3')
makedepends=('git')
depends=()
conflicts=('calamares-net-config')
provides=("${pkgname}")
options=(!strip !emptydirs)
source=("git+https://github.com/Sprunglesonthehub/calamares-config-gnome.git")
sha256sums=('SKIP')

_destname1="/etc"
_destname2="/usr/local/bin"
_destname3="/usr/share/backgrounds"

package() {
  cd "${srcdir}/calamares-config-gnome"

  # Install /etc files
  install -dm755 "${pkgdir}${_destname1}"
  cp -r etc/* "${pkgdir}${_destname1}/"

  # Install /usr/share/backgrounds
  install -dm755 "${pkgdir}${_destname3}"
  cp -r usr/share/backgrounds/* "${pkgdir}${_destname3}/"

  # Optionally install scripts (uncomment if needed)
  # install -dm755 "${pkgdir}${_destname2}"
  # cp -r usr/local/bin/* "${pkgdir}${_destname2}/"
  # chmod +x "${pkgdir}${_destname2}/"*
}
