#
# CDDL HEADER START
#
# The contents of this file are subject to the terms of the
# Common Development and Distribution License (the "License").
# You may not use this file except in compliance with the License.
#
# You can obtain a copy of the license at usr/src/OPENSOLARIS.LICENSE
# or http://www.opensolaris.org/os/licensing.
# See the License for the specific language governing permissions
# and limitations under the License.
#
# When distributing Covered Code, include this CDDL HEADER in each
# file and include the License file at usr/src/OPENSOLARIS.LICENSE.
# If applicable, add the following below this CDDL HEADER, with the
# fields enclosed by brackets "[]" replaced with your own identifying
# information: Portions Copyright [yyyy] [name of copyright owner]
#
# CDDL HEADER END
#

#
# Copyright (c) 2007, 2010, Oracle and/or its affiliates. All rights reserved.
#

#
# Makefile for commands (usr/src/cmd/Makefile)
#

include $(SRC)/Makefile.master

SUBDIRS= auto-install gui-install gui-aux installadm rbac slim-install \
    system-config
PYTHONSUBDIRS= ai-webserver distro_const text-install
TOOLSSUBDIRS= install-tools

.PARALLEL:

all:=		TARGET=	all
check:=		TARGET= check
clean:=		TARGET=	clean
clobber:=	TARGET=	clobber
cstyle:=	TARGET= cstyle
install:=	TARGET=	install
install_h:=	TARGET= install_h
lint:=		TARGET= lint
lintlib:=	TARGET= lintlib
patch:=		TARGET=	install

.KEEP_STATE:

all clean clobber install: $(SUBDIRS) $(PYTHONSUBDIRS) $(TOOLSSUBDIRS)

check cstyle install_h lint lintlib patch: $(SUBDIRS)

headers: install_h

$(SUBDIRS) $(PYTHONSUBDIRS) $(TOOLSSUBDIRS): FRC
	cd $@; pwd; echo $(TARGET); $(MAKE) $(TARGET)

FRC:
