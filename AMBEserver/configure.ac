AC_PREREQ([2.69])
AC_INIT([AMBEserver], [1.1])
AM_INIT_AUTOMAKE([-Wall -Werror -Wno-extra-portability foreign no-define subdir-objects])
m4_ifdef([AM_PROG_AR], [AM_PROG_AR])

AM_MAINTAINER_MODE

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC
AC_PROG_INSTALL
AC_PROG_MAKE_SET
AC_PROG_RANLIB

# Checks for libraries.
PKG_CHECK_MODULES([LIBUSB], [libusb-1.0 >= 1.0.0])

AC_ARG_WITH([gpio],
  [AS_HELP_STRING([--with-gpio],
    [enable support for WiringPi GPIO signalling])],
  [],
  [with_gpio=no])

GPIO=
AS_IF([test "x$with_gpio" != xno],
  [AC_CHECK_LIB([wiringPi], [wiringPiSetup],
    [AC_DEFINE([GPIO])
    AM_CONDITIONAL([WITH_GPIO], true)
    ],
    [AC_MSG_FAILURE(
      [--with-gpio was given but the wiringPi library is not available])],
  )],
  [AM_CONDITIONAL([WITH_GPIO], false)]
)

AM_CONDITIONAL([WITH_AMBESERVER], true)

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
