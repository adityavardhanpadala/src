#	$NetBSD: Makefile,v 1.4 2019/09/26 02:01:03 christos Exp $

.include "../Makefile.inc"
.include "../Makefile.assym"

.PATH:	${S}/compat/netbsd32

KMOD=	compat_netbsd32_16

CPPFLAGS+=	-DCOMPAT_NETBSD32
CPPFLAGS+=	-DCOMPAT_16 -DCOMPAT_20 -DCOMPAT_30
CPPFLAGS+=	-DCOMPAT_40 -DCOMPAT_50 -DCOMPAT_60 -DCOMPAT_70 -DCOMPAT_80
CPPFLAGS+=	-I${NETBSDSRCDIR}/sys/external/bsd/libnv/dist

SRCS+=	netbsd32_compat_16.c

.if ${MACHINE_ARCH} == "x86_64"
.PATH:  ${S}/arch/amd64/amd64
SRCS+=  netbsd32_sigcode.S
SRCS+=	netbsd32_machdep_16.c
.endif

.if ${MACHINE_ARCH} == "arm"
.PATH:	${S}/arch/arm/arm32
SRCS+=	netbsd32_machdep_16.c
.endif

.include <bsd.kmodule.mk>
