# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-catalyst-plugin-datetime'
pkgver='0.03'
pkgrel='1'
pkgdesc=""
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-catalyst-runtime' 'perl-datetime>=0.20')
makedepends=()
url='http://search.cpan.org/dist/Catalyst-Plugin-DateTime'
source=('http://search.cpan.org/CPAN/authors/id/J/JK/JKISER/Catalyst-Plugin-DateTime-0.03.tgz')
md5sums=('3ad09a34f38dd2a34b57deb678c19cdf')
sha512sums=('eb2dd5f23ae5b046bd3931ea31171ac166c27bb012c0df7659ddababd39ebedf9d60d58264e680c951e6e207e099e21f6347bc3311dba54d7784d23c14d5b3d3')
_distdir="Catalyst-Plugin-DateTime-0.03"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
