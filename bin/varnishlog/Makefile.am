#

AM_CPPFLAGS = \
	-I$(top_srcdir)/include \
	-I$(top_builddir)/include

bin_PROGRAMS = varnishlog

varnishlog_SOURCES = \
	varnishlog.c \
	varnishlog_options.h \
	varnishlog_options.c \
	$(top_srcdir)/lib/libvarnishtools/vut.c \
	$(top_srcdir)/lib/libvarnish/vas.c \
	$(top_srcdir)/lib/libvarnish/flopen.c \
	$(top_srcdir)/lib/libvarnish/version.c \
	$(top_srcdir)/lib/libvarnish/vsb.c \
	$(top_srcdir)/lib/libvarnish/vpf.c \
	$(top_srcdir)/lib/libvarnish/vtim.c

varnishlog_CFLAGS = \
	@SAN_CFLAGS@

varnishlog_LDADD = \
	$(top_builddir)/lib/libvarnishcompat/libvarnishcompat.la \
	$(top_builddir)/lib/libvarnishapi/libvarnishapi.la \
	@SAN_LDFLAGS@ \
	${RT_LIBS} ${LIBM} ${PTHREAD_LIBS}

noinst_PROGRAMS = varnishlog_opt2rst
varnishlog_opt2rst_SOURCES = \
	varnishlog_options.h \
	varnishlog_options.c \
	$(top_srcdir)/lib/libvarnishtools/opt2rst.c
