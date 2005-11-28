libmandir = $(LIB_MAN_DIR)

libman_SOURCES = Xcursor.man
libman_DATA = $(libman_SOURCES:man=@LIB_MAN_SUFFIX@)

all-local: $(libman_DATA)

EXTRA_DIST = $(libman_SOURCES)
CLEANFILES = $(libman_DATA)

SUFFIXES = .$(LIB_MAN_SUFFIX) .man

.man.$(LIB_MAN_SUFFIX):
	-rm -f $@
	$(LN_S) $< $@
