#  Copyright (c) 1988, 1989, 1990, 1991, 1992, 1993, 1994, 1995, 1996, 1997
# 	The Regents of the University of California.  All rights reserved.
#
#  Redistribution and use in source and binary forms, with or without
#  modification, are permitted provided that: (1) source code distributions
#  retain the above copyright notice and this paragraph in its entirety, (2)
#  distributions including binary code include the above copyright notice and
#  this paragraph in its entirety in the documentation or other materials
#  provided with the distribution, and (3) all advertising materials mentioning
#  features or use of this software display the following acknowledgement:
#  ``This product includes software developed by the University of California,
#  Lawrence Berkeley Laboratory and its contributors.'' Neither the name of
#  the University nor the names of its contributors may be used to endorse
#  or promote products derived from this software without specific prior
#  written permission.
#  THIS SOFTWARE IS PROVIDED ``AS IS'' AND WITHOUT ANY EXPRESS OR IMPLIED
#  WARRANTIES, INCLUDING, WITHOUT LIMITATION, THE IMPLIED WARRANTIES OF
#  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.

#
# Various configurable paths (remember to edit Makefile.in, not Makefile)
#

# Top level hierarchy
prefix = /usr/local
exec_prefix = ${prefix}
datarootdir = ${prefix}/share
# Pathname of directory to install the binary
sbindir = ${exec_prefix}/sbin
# Pathname of directory to install the man page
mandir = ${datarootdir}/man

# VPATH
srcdir = .


#
# You shouldn't need to edit anything below here.
#

CC = gcc
AR = ar
MKDEP = 
PROG = tcpdump
CCOPT = 
INCLS = -I. -I/usr/local/include 
DEFS = -DHAVE_CONFIG_H   -D_U_="__attribute__((unused))"

# Standard CFLAGS
CFLAGS = -g -O2
FULL_CFLAGS = $(CCOPT) $(DEFS) $(INCLS) $(CFLAGS)

# Standard LDFLAGS
LDFLAGS = 

# Standard LIBS
LIBS = -L/usr/local/lib  -lpcap 

INSTALL = /usr/bin/install -c
INSTALL_PROGRAM = ${INSTALL}
INSTALL_DATA = ${INSTALL} -m 644
RANLIB = ranlib

DEPENDENCY_CFLAG = 

# Explicitly define compilation rule since SunOS 4's make doesn't like gcc.
# Also, gcc does not remove the .o before forking 'as', which can be a
# problem if you don't own the file but can write to the directory.
.c.o:
	@rm -f $@
	$(CC) $(FULL_CFLAGS) -c $(srcdir)/$*.c

CSRC =	setsignal.c tcpdump.c

LIBNETDISSECT_SRC=\
	addrtoname.c \
	addrtostr.c \
	af.c \
	ascii_strcasecmp.c \
	checksum.c \
	cpack.c \
	gmpls.c \
	gmt2local.c \
	in_cksum.c \
	ipproto.c \
	l2vpn.c \
	machdep.c \
	nlpid.c \
	oui.c \
	parsenfsfh.c \
	print.c \
	print-802_11.c \
	print-802_15_4.c \
	print-ah.c \
	print-ahcp.c \
	print-aodv.c \
	print-aoe.c \
	print-ap1394.c \
	print-arcnet.c \
	print-arp.c \
	print-ascii.c \
	print-atalk.c \
	print-atm.c \
	print-babel.c \
	print-beep.c \
	print-bfd.c \
	print-bgp.c \
	print-bootp.c \
	print-bt.c \
	print-calm-fast.c \
	print-carp.c \
	print-cdp.c \
	print-cfm.c \
	print-chdlc.c \
	print-cip.c \
	print-cnfp.c \
	print-dccp.c \
	print-decnet.c \
	print-dhcp6.c \
	print-domain.c \
	print-dtp.c \
	print-dvmrp.c \
	print-eap.c \
	print-egp.c \
	print-eigrp.c \
	print-enc.c \
	print-esp.c \
	print-ether.c \
	print-fddi.c \
	print-forces.c \
	print-fr.c \
	print-frag6.c \
	print-ftp.c \
	print-geneve.c \
	print-geonet.c \
	print-gre.c \
	print-hncp.c \
	print-hsrp.c \
	print-http.c \
	print-icmp.c \
	print-icmp6.c \
	print-igmp.c \
	print-igrp.c \
	print-ip.c \
	print-ip6.c \
	print-ip6opts.c \
	print-ipcomp.c \
	print-ipfc.c \
	print-ipnet.c \
	print-ipx.c \
	print-isakmp.c \
	print-isoclns.c \
	print-juniper.c \
	print-krb.c \
	print-l2tp.c \
	print-lane.c \
	print-ldp.c \
	print-lisp.c \
	print-llc.c \
	print-lldp.c \
	print-lmp.c \
	print-loopback.c \
	print-lspping.c \
	print-lwapp.c \
	print-lwres.c \
	print-m3ua.c \
	print-medsa.c \
	print-mobile.c \
	print-mobility.c \
	print-mpcp.c \
	print-mpls.c \
	print-mptcp.c \
	print-msdp.c \
	print-msnlb.c \
	print-nflog.c \
	print-nfs.c \
	print-nsh.c \
	print-ntp.c \
	print-null.c \
	print-olsr.c \
	print-openflow-1.0.c \
	print-openflow.c \
	print-ospf.c \
	print-ospf6.c \
	print-otv.c \
	print-pgm.c \
	print-pim.c \
	print-pktap.c \
	print-ppi.c \
	print-ppp.c \
	print-pppoe.c \
	print-pptp.c \
	print-radius.c \
	print-raw.c \
	print-resp.c \
	print-rip.c \
	print-ripng.c \
	print-rpki-rtr.c \
	print-rrcp.c \
	print-rsvp.c \
	print-rt6.c \
	print-rtsp.c \
	print-rx.c \
	print-sctp.c \
	print-sflow.c \
	print-sip.c \
	print-sl.c \
	print-sll.c \
	print-slow.c \
	print-smtp.c \
	print-snmp.c \
	print-stp.c \
	print-sunatm.c \
	print-sunrpc.c \
	print-symantec.c \
	print-syslog.c \
	print-tcp.c \
	print-telnet.c \
	print-tftp.c \
	print-timed.c \
	print-tipc.c \
	print-token.c \
	print-udld.c \
	print-udp.c \
	print-usb.c \
	print-vjc.c \
	print-vqp.c \
	print-vrrp.c \
	print-vtp.c \
	print-vxlan.c \
	print-vxlan-gpe.c \
	print-wb.c \
	print-zephyr.c \
	print-zeromq.c \
	netdissect.c \
	signature.c \
	strtoaddr.c \
	util-print.c

LOCALSRC = 
GENSRC = version.c
LIBOBJS = 

LIBNETDISSECT_OBJ=$(LIBNETDISSECT_SRC:.c=.o) ${LOCALSRC:.c=.o} ${LIBOBJS}
LIBNETDISSECT=libnetdissect.a


SRC =	$(CSRC) $(GENSRC) $(LOCALSRC) $(LIBNETDISSECT_SRC)

# We would like to say "OBJ = $(SRC:.c=.o)" but Ultrix's make cannot
# hack the extra indirection
OBJ =	$(CSRC:.c=.o) $(GENSRC:.c=.o) $(LIBNETDISSECT_OBJ)
HDR = \
	addrtoname.h \
	addrtostr.h \
	af.h \
	ah.h \
	appletalk.h \
	ascii_strcasecmp.h \
	atm.h \
	chdlc.h \
	cpack.h \
	ether.h \
	ethertype.h \
	extract.h \
	funcattrs.h \
	getopt_long.h \
	gmpls.h \
	gmt2local.h \
	interface.h \
	ip.h \
	ip6.h \
	ipproto.h \
	l2vpn.h \
	llc.h \
	machdep.h \
	mib.h \
	mpls.h \
	nameser.h \
	netdissect.h \
	nfs.h \
	nfsfh.h \
	nlpid.h \
	openflow.h \
	ospf.h \
	oui.h \
	pcap-missing.h \
	ppp.h \
	print.h \
	rpc_auth.h \
	rpc_msg.h \
	rpl.h \
	setsignal.h \
	signature.h \
	slcompress.h \
	smb.h \
	strtoaddr.h \
	tcp.h \
	netdissect-stdinc.h \
	timeval-operations.h \
	udp.h

TAGHDR = \
	/usr/include/arpa/tftp.h \
	/usr/include/net/if_arp.h \
	/usr/include/netinet/if_ether.h \
	/usr/include/netinet/in.h \
	/usr/include/netinet/ip_icmp.h \
	/usr/include/netinet/tcp.h \
	/usr/include/netinet/udp.h \
	/usr/include/protocols/routed.h

TAGFILES = $(SRC) $(HDR) $(TAGHDR)

CLEANFILES = $(PROG) $(OBJ) $(GENSRC)

EXTRA_DIST = \
	CHANGES \
	CONTRIBUTING \
	CREDITS \
	INSTALL.txt \
	LICENSE \
	Makefile.in \
	Makefile-devel-adds \
	PLATFORMS \
	README \
	README.md \
	Readme.Win32 \
	VERSION \
	aclocal.m4 \
	atime.awk \
	bpf_dump.c \
	config.guess \
	config.h.in \
	config.sub \
	configure \
	configure.ac \
	install-sh \
	lbl/os-osf4.h \
	lbl/os-solaris2.h \
	lbl/os-sunos4.h \
	lbl/os-ultrix4.h \
	makemib \
	missing/dlnames.c \
	missing/datalinks.c \
	missing/getopt_long.c \
	missing/snprintf.c \
	missing/strdup.c \
	missing/strlcat.c \
	missing/strlcpy.c \
	missing/strsep.c \
	mkdep \
	packetdat.awk \
	pcap_dump_ftell.c \
	print-pflog.c \
	print-smb.c \
	send-ack.awk \
	smbutil.c \
	stime.awk \
	tcpdump.1.in \
	vfprintf.c \
	win32/prj/GNUmakefile \
	win32/prj/WinDump.dsp \
	win32/prj/WinDump.dsw \
	win32/prj/WinDump.sln \
	win32/prj/WinDump.vcproj \
	win32/src/ether_ntohost.c

TEST_DIST= `git ls-files tests | grep -v 'tests/\..*'`

all: $(PROG) $(LIBNETDISSECT)

$(PROG): $(OBJ) 
	@rm -f $@
	$(CC) $(FULL_CFLAGS) $(LDFLAGS) -o $@ $(OBJ) $(LIBS)

$(LIBNETDISSECT): $(LIBNETDISSECT_OBJ)
	@rm -f $@
	$(AR) cr $@ $(LIBNETDISSECT_OBJ)
	$(RANLIB) $@

datalinks.o: $(srcdir)/missing/datalinks.c
	$(CC) $(FULL_CFLAGS) -o $@ -c $(srcdir)/missing/datalinks.c
dlnames.o: $(srcdir)/missing/dlnames.c
	$(CC) $(FULL_CFLAGS) -o $@ -c $(srcdir)/missing/dlnames.c
getopt_long.o: $(srcdir)/missing/getopt_long.c
	$(CC) $(FULL_CFLAGS) -o $@ -c $(srcdir)/missing/getopt_long.c
snprintf.o: $(srcdir)/missing/snprintf.c
	$(CC) $(FULL_CFLAGS) -o $@ -c $(srcdir)/missing/snprintf.c
strdup.o: $(srcdir)/missing/strdup.c
	$(CC) $(FULL_CFLAGS) -o $@ -c $(srcdir)/missing/strdup.c
strlcat.o: $(srcdir)/missing/strlcat.c
	$(CC) $(FULL_CFLAGS) -o $@ -c $(srcdir)/missing/strlcat.c
strlcpy.o: $(srcdir)/missing/strlcpy.c
	$(CC) $(FULL_CFLAGS) -o $@ -c $(srcdir)/missing/strlcpy.c
strsep.o: $(srcdir)/missing/strsep.c
	$(CC) $(FULL_CFLAGS) -o $@ -c $(srcdir)/missing/strsep.c

version.o: version.c
	$(CC) $(FULL_CFLAGS) -c version.c

version.c: $(srcdir)/VERSION
	@rm -f $@
	if grep GIT ${srcdir}/VERSION >/dev/null; then \
		read ver <${srcdir}/VERSION; \
		echo $$ver | tr -d '\012'; \
		date +_%Y_%m_%d; \
	else \
		cat ${srcdir}/VERSION; \
	fi | sed -e 's/.*/const char version[] = "&";/' > $@

install: all
	[ -d $(DESTDIR)$(sbindir) ] || \
	    (mkdir -p $(DESTDIR)$(sbindir); chmod 755 $(DESTDIR)$(sbindir))
	$(INSTALL_PROGRAM) $(PROG) $(DESTDIR)$(sbindir)/$(PROG)
	$(INSTALL_PROGRAM) $(PROG) $(DESTDIR)$(sbindir)/$(PROG).`cat ${srcdir}/VERSION`
	[ -d $(DESTDIR)$(mandir)/man1 ] || \
	    (mkdir -p $(DESTDIR)$(mandir)/man1; chmod 755 $(DESTDIR)$(mandir)/man1)
	$(INSTALL_DATA) $(PROG).1 $(DESTDIR)$(mandir)/man1/$(PROG).1

uninstall:
	rm -f $(DESTDIR)$(sbindir)/$(PROG)
	rm -f $(DESTDIR)$(mandir)/man1/$(PROG).1

lint: $(GENSRC)
	lint -hbxn $(SRC) | \
	    grep -v 'struct/union .* never defined' | \
	    grep -v 'possible pointer alignment problem'

clean:
	rm -f $(CLEANFILES) $(PROG)-`cat VERSION`.tar.gz

distclean:
	rm -f $(CLEANFILES) Makefile config.cache config.log config.status \
	    config.h gnuc.h os-proto.h stamp-h stamp-h.in $(PROG).1 \
	    libnetdissect.a tests/.failed tests/.passed \
	    tests/failure-outputs.txt
	rm -rf autom4te.cache tests/DIFF tests/NEW

check: tcpdump
	(mkdir -p tests && SRCDIR=`cd ${srcdir}; pwd` && export SRCDIR && $$SRCDIR/tests/TESTrun.sh )

extags: $(TAGFILES)
	ctags $(TAGFILES)

tags: $(TAGFILES)
	ctags -wtd $(TAGFILES)

TAGS: $(TAGFILES)
	etags $(TAGFILES)

releasetar:
	@cwd=`pwd` ; dir=`basename $$cwd` ; name=$(PROG)-`cat VERSION` ; \
	   mkdir $$name; \
	   tar cf - $(CSRC) $(HDR) $(LIBNETDISSECT_SRC) $(EXTRA_DIST) $(TEST_DIST) | (cd $$name; tar xf -); \
	   tar -c -z -f $$name.tar.gz $$name; \
	   rm -rf $$name

testlist:
	echo $(TEST_DIST)

depend: $(GENSRC)
	$(MKDEP) -c $(CC) -m $(DEPENDENCY_CFLAG) $(DEFS) $(INCLS) $(SRC)
