noinst_HEADERS = socket.h name.h

rpctransport_LTLIBRARIES = socket.la
rpctransportdir = $(libdir)/glusterfs/$(PACKAGE_VERSION)/rpc-transport

socket_la_LDFLAGS = -module -avoidversion

socket_la_SOURCES = socket.c name.c
socket_la_LIBADD = $(top_builddir)/libglusterfs/src/libglusterfs.la -lssl

AM_CPPFLAGS = $(GF_CPPFLAGS) \
	-I$(top_srcdir)/libglusterfs/src -I$(top_srcdir)/rpc/rpc-lib/src/ \
	-I$(top_srcdir)/rpc/xdr/src/

AM_CFLAGS = -Wall $(GF_CFLAGS)

CLEANFILES = *~
