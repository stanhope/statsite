AC_INIT(statsite, 0.1, me@somebody.com)

AC_CONFIG_AUX_DIR(config)

AC_CONFIG_SRCDIR(src/statsite.c)

AM_INIT_AUTOMAKE([subdir-objects])

AC_PROG_CC

# libev (which shouldn't use pkg-config anyways, but has
#   to on Fedora because they munge the header path the author intended...)
PKG_CHECK_MODULES([LIBEV],[libev >= 4.0],
    CPPFLAGS="${CPPFLAGS} ${LIBEV_CFLAGS}"
,
    # try manually...
    XLIBS=$LIBS
    LIBS=""
    AC_CHECK_LIB([ev],[ev_break],,AC_MSG_ERROR([libev 4.x library not found!]))
    AC_CHECK_DECLS([EVBREAK_ALL],,AC_MSG_ERROR([libev 4.x headers not found!]),[
        #include <ev.h>
    ])
    LIBEV_LIBS=$LIBS
    LIBS=$XLIBS
)
AC_SUBST([LIBEV_LIBS])

AC_OUTPUT(Makefile src/Makefile)
