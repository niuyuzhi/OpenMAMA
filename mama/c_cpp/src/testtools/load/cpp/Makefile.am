# $Id$
#
# OpenMAMA: The open middleware agnostic messaging API
# Copyright (C) 2011 NYSE Technologies, Inc.
#
# This library is free software; you can redistribute it and/or
# modify it under the terms of the GNU Lesser General Public
# License as published by the Free Software Foundation; either
# version 2.1 of the License, or (at your option) any later version.
#
# This library is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
# Lesser General Public License for more details.
#
# You should have received a copy of the GNU Lesser General Public
# License along with this library; if not, write to the Free Software
# Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA
# 02110-1301 USA
#

mama_platform = @mama_platform@
srcdir        = @srcdir@
blddir        = @builddir@
VPATH         = @srcdir@

INCLUDES = -I$(srcdir) \
           -I$(prefix)/include \
           -I$(srcdir)/../../../c \
           -I$(srcdir)/../../../cpp \
           -I${srcdir}/../../../../../../common/c_cpp/src/c \
           -I${srcdir}/../../../../../../common/c_cpp/src/cpp \
           -I${srcdir}/.. \
           -I${srcdir}/../..
            

LDFLAGS += -L${srcdir}/../../../c \
           -L${srcdir}/../../../cpp \
           -L${srcdir}/../../../../../../common/c_cpp/src/c \
           -L${srcdir}/../../../../../../common/c_cpp/src/cpp \
           -L${srcdir}/.. \
           -L${srcdir}/../..

if USE_GCC_FLAGS
CFLAGS   += -std=gnu99 -pedantic-errors -Wmissing-prototypes -Wstrict-prototypes
CPPFLAGS += -pedantic-errors -Wall -Wimplicit -Wno-long-long -D_GNU_SOURCE
endif

CFLAGS    += -I@builddir@/../../c
CPPFLAGS  += -I@builddir@/../../cpp


LDADD     =  -lmamacpp -lmama -lpthread -ldl


bin_PROGRAMS = mamachurncpp

nodist_mamachurncpp_SOURCES = mamachurncpp.cpp
