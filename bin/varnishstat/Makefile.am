#

AM_CPPFLAGS = \
	-I$(top_srcdir)/include \
	-I$(top_builddir)/include

bin_PROGRAMS = varnishstat

varnishstat_SOURCES = \
	varnishstat.h \
	\
	varnishstat.c \
	varnishstat_curses.c \
	$(top_srcdir)/lib/libvarnish/vas.c \
	$(top_srcdir)/lib/libvarnish/version.c \
	$(top_srcdir)/lib/libvarnish/vtim.c

varnishstat_CFLAGS = \
	@SAN_CFLAGS@

varnishstat_LDADD = \
	$(top_builddir)/lib/libvarnishcompat/libvarnishcompat.la \
	$(top_builddir)/lib/libvarnishapi/libvarnishapi.la \
	@SAN_LDFLAGS@ \
	@CURSES_LIB@ ${RT_LIBS} ${LIBM} ${PTHREAD_LIBS}

noinst_PROGRAMS = vsc2rst
vsc2rst_SOURCES = vsc2rst.c $(top_srcdir)/include/tbl/vsc_fields.h
