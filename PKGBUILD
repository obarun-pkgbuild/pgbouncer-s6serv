# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=pgbouncer-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="pgbouncer service for s6"
arch=(x86_64)
license=('beerware')
depends=('pgbouncer' 's6' 's6-rc' 's6-boot')
conflicts=()
install=pgbouncer-s6serv.install
source=('pgbouncer.daemon.run.s6'
		'pgbouncer.log.run.s6'
		'LICENSE')
md5sums=('b53146a039d962871901c6d5b8f7ac98'
         '6947f20655bf53fd572f265d19813d17'
         '191a37ae657aa17e37e75d0242865dba')


package() {
	
	# daemon
	install -Dm 0755 "$srcdir/pgbouncer.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/pgbouncer/run"
	
	# log
	install -Dm 0755 "$srcdir/pgbouncer.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/pgbouncer/log/run"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/pgbouncer-s6serv/LICENSE"
}
