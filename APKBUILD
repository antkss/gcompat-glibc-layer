#!/bin/bash
pkgname=gcompat
pkgver=2.0.0
pkgrel=1
pkgdesc="hyprdepen"
arch="x86_64"
license="BSD"
depends="py3-build py3-installer poetry"
url="google.com"
export bdir=$srcdir/..

prepare() {
	cd $bdir

}

build() {
	cd $bdir/$pkgname
	make
}

package() {
	cd $bdir/$pkgname
	# install -D -m755 libc.so.6 $pkgdir/usr/lib/libc.so.6
	# install -D -m755 ld-linux-x86-64.so.2 $pkgdir/usr/lib/ld-linux-x86-64.so.2
	# mkdir -p $pkgdir/lib
	# ln -s /usr/lib/libc.so.6 $pkgdir/lib/libc.so.6
	# ln -s /usr/lib/ld-linux-x86-64.so.2 $pkgdir/lib/ld-linux-x86-64.so.2
	# mkdir -p $pkgdir/lib64
	# ln -s /usr/lib/libc.so.6 $pkgdir/lib64/libc.so.6
	# ln -s /usr/lib/ld-linux-x86-64.so.2 $pkgdir/lib64/ld-linux-x86-64.so.2
	make DESTDIR=$pkgdir install
	# cp libc.so.6 ld-linux-x86-64.so.2 $pkgdir

}
