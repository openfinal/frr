## Process this file with automake to produce Makefile.in.

AM_CPPFLAGS = -I.. -I$(top_srcdir) -I$(top_srcdir)/lib -I$(top_builddir)/lib -DQUAGGA_NO_DEPRECATED_INTERFACES
DEFS = @DEFS@ @CARES_CFLAGS@ -DSYSCONFDIR=\"$(sysconfdir)/\"
INSTALL_SDATA=@INSTALL@ -m 600

AM_CFLAGS = $(PICFLAGS) #$(WERROR)
AM_LDFLAGS = $(PICLDFLAGS)

sbin_PROGRAMS = nhrpd

nhrpd_SOURCES = \
	zbuf.c \
	znl.c \
	resolver.c \
	linux.c \
	netlink_arp.c \
	netlink_gre.c \
	vici.c \
	reqid.c \
	nhrp_event.c \
	nhrp_packet.c \
	nhrp_interface.c \
	nhrp_vc.c \
	nhrp_peer.c \
	nhrp_cache.c \
	nhrp_nhs.c \
	nhrp_route.c \
	nhrp_shortcut.c \
	nhrp_vty.c \
	nhrp_main.c

nhrpd_LDADD = ../lib/libfrr.la @LIBCAP@ @CARES_LIBS@

noinst_HEADERS = \
	debug.h \
	list.h \
	netlink.h \
	nhrp_protocol.h \
	nhrpd.h \
	os.h \
	vici.h \
	zbuf.h \
	znl.h \
	# end

#dist_examples_DATA = nhrpd.conf.sample
