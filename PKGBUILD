# Maintainer: Frederik Schwan <frederik dot schwan at linux dot com>

pkgname=imapsync
pkgver=1.882
pkgrel=2
pkgdesc='IMAP synchronisation, sync, copy or migration tool'
arch=('any')
url='http://www.linux-france.org/prj/'
license=('GPL')
depends=('cpanminus' 'perl-cgi' 'perl-crypt-openssl-rsa' 'perl-data-uniqid' 'perl-date-manip'
        'perl-file-copy-recursive' 'perl-html-parser' 'perl-io-socket-inet6' 'perl-io-socket-ssl'
        'perl-io-tee' 'perl-json-webtoken' 'perl-libwww' 'perl-module-scandeps'
        'perl-mail-imapclient' 'perl-module-runtime' 'perl-ntlm' 'perl-package-stash'
        'perl-par-packer' 'perl-readonly' 'perl-regexp-common' 'perl-sys-meminfo'
        'perl-term-readkey' 'perl-test-deep' 'perl-test-fatal' 'perl-test-mock-guard'
        'perl-test-mockobject' 'perl-test-pod' 'perl-test-requires' 'perl-test-warn'
        'perl-unicode-string')
source=(https://github.com/imapsync/imapsync/archive/${pkgname}-${pkgver}.tar.gz)
sha512sums=('3953cb29b210c283be3fe72f1e1537594415bd5457b469b801625d6c857b982d2b2b3da9528dd1e6ccc6831c022ce495f7a5eaaea04d228bca374f185344f455')

build() {
  cd "${srcdir}/${pkgname}-${pkgname}-${pkgver}"
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
