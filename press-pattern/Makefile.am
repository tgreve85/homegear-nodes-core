AUTOMAKE_OPTIONS = subdir-objects

AM_CPPFLAGS = -Wall -std=c++11 -DFORTIFY_SOURCE=2 -DGCRYPT_NO_DEPRECATED
AM_LDFLAGS = -Wl,-rpath=/lib/homegear -Wl,-rpath=/usr/lib/homegear -Wl,-rpath=/usr/local/lib/homegear
LIBS += -Wl,-Bdynamic -lhomegear-node

libdir = $(localstatedir)/lib/homegear/node-blue/nodes/press-pattern
lib_LTLIBRARIES = press-pattern.la
press_pattern_la_SOURCES = Factory.cpp MyNode.cpp
press_pattern_la_LDFLAGS =-module -avoid-version -shared
press_pattern_ladir = $(libdir)
press_pattern_la_DATA = press-pattern.hni
locale_en_usdir = $(libdir)/locales/en-US
locale_en_us_DATA = locales/en-US/press-pattern
install-exec-hook:
	rm -f $(DESTDIR)$(libdir)/press-pattern.la
