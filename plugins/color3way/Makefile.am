plugin_LTLIBRARIES = color3way.la
color3way_la_LDFLAGS = -avoid-version -module -shared
color3way_la_LIBADD =
color3way_la_SOURCES = \
	aggregated.h \
	color3way.C \
	color3way.h \
	color3waywindow.C \
	color3waywindow.h

AM_CXXFLAGS = $(LARGEFILE_CFLAGS)

AM_CPPFLAGS = -I$(top_srcdir)/guicast -I$(top_srcdir)/cinelerra -I$(top_srcdir)/quicktime
LIBTOOL = $(SHELL) $(top_builddir)/libtool $(LTCXX_FLAGS)

#BUILT_SOURCES = picon_png.h
#picon_png.h: picon.png
#	$(top_builddir)/guicast/pngtoh $^ || { rm -f $@; exit 1; }
#clean-local:
#	$(RM) picon_png.h
