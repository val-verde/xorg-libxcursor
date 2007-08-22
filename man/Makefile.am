libmandir = $(LIB_MAN_DIR)

libman_PRE = Xcursor.man
libman_DATA = $(libman_PRE:man=@LIB_MAN_SUFFIX@)

all-local: $(libman_DATA)

EXTRA_DIST = $(libman_PRE)
CLEANFILES = $(libman_DATA)

SUFFIXES = .$(LIB_MAN_SUFFIX) .man

# Strings to replace in man pages
XORGRELSTRING = @PACKAGE_STRING@

MAN_SUBSTS = \
	-e 's|__xorgversion__|"$(XORGRELSTRING)"|' \
	-e 's|__XCURSORPATH__|$(XCURSORPATH_LIST)|g' \
	-e 's|__appmansuffix__|$(APP_MAN_SUFFIX)|g' \
	-e 's|__libmansuffix__|$(LIB_MAN_SUFFIX)|g' \
	-e 's|__adminmansuffix__|$(ADMIN_MAN_SUFFIX)|g' \
	-e 's|__miscmansuffix__|$(MISC_MAN_SUFFIX)|g' \
	-e 's|__filemansuffix__|$(FILE_MAN_SUFFIX)|g'

.man.$(LIB_MAN_SUFFIX):
	-rm -f $@
	sed $(MAN_SUBSTS) < $< > $@
