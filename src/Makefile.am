lib_LTLIBRARIES = libXcursor.la

libXcursor_la_SOURCES = xcursorint.h cursor.c display.c file.c library.c xlib.c

libXcursor_la_LIBADD = $(XRENDER_LIBS) $(XFIXES_LIBS) $(X_LIBS)
AM__CFLAGS = $(XRENDER_CFLAGS) $(XFIXES_CFLAGS) $(X_CFLAGS)

INCLUDES = -I$(top_srcdir)/include/X11/Xcursor

#
# Shared library version info.  This is not the same as the package version
#
libXcursor_la_LDFLAGS = -version-info @LT_VERSION_INFO@ -no-undefined

libXcursorincludedir = $(includedir)/X11/Xcursor
libXcursorinclude_HEADERS = $(top_srcdir)/include/X11/Xcursor/Xcursor.h 
