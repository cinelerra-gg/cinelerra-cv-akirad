plugin_LTLIBRARIES = titler.la
titler_la_LDFLAGS = -avoid-version -module -shared 
titler_la_LIBADD = $(top_builddir)/plugins/colors/libcolors.la -lfreetype -lfontconfig
titler_la_SOURCES = title.C titlewindow.C 
AM_CXXFLAGS = $(LARGEFILE_CFLAGS)

AM_CPPFLAGS = -I$(top_srcdir)/guicast -I$(top_srcdir)/cinelerra -I$(top_srcdir)/quicktime ${FREETYPE_CFLAGS} -I$(top_srcdir)/plugins/colors
LIBTOOL = $(SHELL) $(top_builddir)/libtool $(LTCXX_FLAGS)

noinst_HEADERS = title.h titlewindow.h 
EXTRA_DIST = picon.png

BUILT_SOURCES = picon_png.h
picon_png.h: picon.png
	$(top_builddir)/guicast/pngtoh $^ || { rm -f $@; exit 1; }
clean-local:
	$(RM) picon_png.h
