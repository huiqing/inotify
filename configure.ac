AC_INIT(erlang binding to inotify, 0.30, mats.cronqvist()gmail.com, inotify)

dnl Require autoconf version >=2.59c. first one with erlang macros
AC_PREREQ(2.59c)
AC_COPYRIGHT(Copyright (C) 2010 Jeff Miller et al)
dnl AC_REVISION($Id$)

dnl Require automake version >=1.9.5.
AM_INIT_AUTOMAKE(1.9.5)

AC_PROG_CC(gcc)
AM_PROG_CC_C_O

dnl Erlang-related configuration.
AC_ERLANG_SUBST_ROOT_DIR
AC_ERLANG_SUBST_LIB_DIR
AC_ERLANG_CHECK_LIB(erl_interface)
AC_ERLANG_SUBST_INSTALL_LIB_SUBDIR(AC_PACKAGE_TARNAME, AC_PACKAGE_VERSION)
erlcflags="+warn_unused_import +warn_obsolete_guard +debug_info"
AC_SUBST([ERLCFLAGS], [$erlcflags])

dnl Specify the files to instantiate.
AC_CONFIG_FILES([ \
	Makefile \
	src/Makefile \
        c_src/Makefile \
	])

AC_OUTPUT
