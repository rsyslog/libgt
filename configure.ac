#
# $Id: configure.ac 123 2011-12-07 23:05:50Z ahto.truu $
#
# Copyright 2009-2010 GuardTime AS
#
# This file is part of the GuardTime client SDK.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#     http://www.apache.org/licenses/LICENSE-2.0
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
# implied. See the License for the specific language governing
# permissions and limitations under the License. 
#
#
# This is the GNU automake configuration script.
# If you don't have the configure script or want to re-generate it
# for some reason, issue
#     aclocal && automake -a && autoconf
#

AC_INIT(libgt, 0.3.11.master, beta_support@guardtime.com)
AC_CONFIG_AUX_DIR(config)

AM_INIT_AUTOMAKE(libgt, 0.3.11)
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

# Checks for programs.
AC_PROG_CC
AC_PROG_LIBTOOL

# Checks for libraries.
AC_CHECK_LIB([crypto], [SHA256_Init], [], [AC_MSG_FAILURE([Could not find OpenSSL 0.9.8+ libraries])])
AC_CHECK_LIB([curl], [curl_global_init], [], [AC_MSG_FAILURE([Could not find cURL libraries])])

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_CONFIG_FILES([libgt.pc])
AC_CONFIG_MACRO_DIR([m4])
AC_OUTPUT(GNUmakefile src/base/GNUmakefile src/http/GNUmakefile src/png/GNUmakefile doc/GNUmakefile)
