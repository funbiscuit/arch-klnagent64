pkgname=('klnagent64')
pkgver=15.1.0.11795
_pkgverbuild=$(echo ${pkgver} | cut -d "." -f 4)
_pkgver=$(echo ${pkgver} | cut -d "." -f 1-3)
pkgrel=1
arch=('x86_64')
pkgdesc="The Kaspersky Network Agent"
url=''
license=('custom')
noextract=("klnagent64_${_pkgver}-${_pkgverbuild}_amd64.deb")
depends=('kesl')
options=('!strip' '!emptydirs')
install=${pkgname}.install
source=( "https://products.s.kaspersky-labs.com/administrationkit/ksc10/${pkgver}/english-19260948-en/3837363732347c44454c7c31/klnagent64_${_pkgver}-${_pkgverbuild}_amd64.deb"
         "${pkgname}.install")
sha256sums=('9316c304ea7028957bf8fd60341c829ccefd2a57b7e3c14af36aa31a4a661710'
            '4b1070ec0e4845ad4c0336bca0e162edda2fea65efd147249d96ee60b4b86f30')

package(){
    bsdtar -xf klnagent64_${_pkgver}-${_pkgverbuild}_amd64.deb
    bsdtar -xf data.tar.gz -C ${pkgdir}/
}
