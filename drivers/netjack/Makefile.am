MAINTAINCLEANFILES = Makefile.in

AM_CFLAGS = $(JACK_CFLAGS)


plugindir = $(ADDON_DIR)

plugin_LTLIBRARIES = jack_net.la

jack_net_la_LDFLAGS = -module -avoid-version @NETJACK_LIBS@
jack_net_la_CFLAGS = @NETJACK_CFLAGS@
jack_net_la_SOURCES = net_driver.c netjack_packet.c netjack.c
jack_net_la_LIBADD = $(top_builddir)/libjack/libjack.la $(top_builddir)/jackd/libjackserver.la

noinst_HEADERS = netjack.h net_driver.h netjack_packet.h

noinst_LTLIBRARIES = libnetjack_packet.la

libnetjack_packet_la_LDFLAGS = @NETJACK_LIBS@
libnetjack_packet_la_CFLAGS = @NETJACK_CFLAGS@
libnetjack_packet_la_SOURCES = netjack_packet.c
