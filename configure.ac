AC_INIT([sugar-base],[0.98.0],[],[sugar-base])

AC_PREREQ([2.59])

AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_SRCDIR([configure.ac])

AM_INIT_AUTOMAKE([1.9 foreign dist-bzip2 no-dist-gzip])

AC_DISABLE_STATIC
AC_PROG_LIBTOOL

GNOME_COMPILE_WARNINGS(maximum)

PYTHON=python2
AM_PATH_PYTHON
AM_CHECK_PYTHON_HEADERS(,[AC_MSG_ERROR(could not find Python headers)])

AC_PATH_PROG(PYGTK_CODEGEN, pygtk-codegen-2.0, no)

PKG_CHECK_MODULES(EXTENSION, pygobject-2.0)

# Setup GETTEXT
#
ALL_LINGUAS="af am ar aym bg bn bn_IN ca de dz el en es fa fa_AF ff fr gu ha hi ht ig is it ja km ko mk ml mn mr mvo nb ne nl pa pap pl ps pt pt_BR quz ro ru rw sd si sl te th tr ur vi yo zh_CN zh_TW"

GETTEXT_PACKAGE=sugar-base
AC_PROG_INTLTOOL([0.33])
AC_SUBST(GETTEXT_PACKAGE)
AC_DEFINE_UNQUOTED(GETTEXT_PACKAGE, "$GETTEXT_PACKAGE", [Gettext package])
AM_GLIB_GNU_GETTEXT

AC_OUTPUT([
Makefile
src/Makefile
src/sugar/Makefile
src/sugar/dispatch/Makefile
po/Makefile.in
])
