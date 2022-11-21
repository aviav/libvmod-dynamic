AM_CFLAGS = $(VARNISHAPI_CFLAGS) -Wall -Werror
AM_LDFLAGS = $(VARNISHAPI_LIBS) $(VMOD_LDFLAGS)

vmod_LTLIBRARIES = libvmod_dynamic.la

libvmod_dynamic_la_SOURCES = \
	vmod_dynamic.h \
	vmod_dynamic.c

nodist_libvmod_dynamic_la_SOURCES = \
	vcc_dynamic_if.c \
	vcc_dynamic_if.h

dist_man_MANS = vmod_dynamic.3

pdf-local: vmod_dynamic.pdf

.rst.pdf:
	rst2pdf $< $@

@BUILD_VMOD_DYNAMIC@
