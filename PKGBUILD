# Maintainer: Cauvmou <cauvmou.8855@gmail.com>
pkgname='ryujinx-ava-ldn-bin'
pkgver='1.1.0_avaldn3.1.3'
pkgrel='3'
pkgdesc='Experimental Nintendo Switch Emulator written in C# (LDN build, test ava build)'
arch=('x86_64')
url='https://www.patreon.com/ryujinx'
license=('MIT')
depends=('dotnet-runtime>=5')
provides=('ryujinx')
conflicts=('ryujinx' 'ryujinx-git' 'ryujinx-ldn-bin' 'ryujinx-ava-bin' 'ryujinx-bin')
options=('!strip')
source=('https://www.patreon.com/file?h=74910544&i=13368553'
        'https://github.com/Ryujinx/Ryujinx/raw/master/src/Ryujinx/Ryujinx.ico'
        'ryujinx.desktop')
b2sums=('ed8d99635b9a1259491a08adace7eccb3a63d3ea592130458410f89ee62d65d0f02d453241cadca5e214943a4d01fbc30e6910c06c3debf430fc38c515a90847'
        '2c092c895b0fb9ea5214fa9366264801c885d8a3f68cf8aa08b66b2c561b976e6000a9eb94080cceb23d5a69cfbc9eebf80cf8a21d0ae7bb060a32947028b698'
        '5e947c80ced8feea52dddeb50d6b8980e2d6c93fe50c612df5cb587a0ebb4cbedf27c49682b3f84f5e6cea20cd83915a070b224951961c8aa1c0504aadc8c0e9')

package() {
    install -d "${pkgdir}/usr/bin/"
    install -dm777 "${pkgdir}/opt/${pkgname}/Logs/"
    install -Dm644 -t "${pkgdir}/opt/${pkgname}/" "${srcdir}/Ryujinx.ico"
    install -Dm644 -t "${pkgdir}/usr/share/applications/" "${srcdir}/ryujinx.desktop"
    cp -r "${srcdir}/publish/"* "${pkgdir}/opt/${pkgname}/"
    ln -s "/opt/${pkgname}/Ryujinx.Ava" "${pkgdir}/usr/bin"
}
