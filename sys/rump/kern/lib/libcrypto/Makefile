#	$NetBSD: Makefile,v 1.6 2019/12/05 03:57:55 riastradh Exp $
#

.PATH:	${.CURDIR}/../../../../crypto/blowfish				\
	${.CURDIR}/../../../../crypto/camellia				\
	${.CURDIR}/../../../../crypto/cast128				\
	${.CURDIR}/../../../../crypto/des				\
	${.CURDIR}/../../../../crypto/rijndael				\
	${.CURDIR}/../../../../crypto/skipjack

LIB=	rumpkern_crypto
COMMENT=Cryptographic routines

# blowfish
SRCS+=	bf_ecb.c bf_enc.c bf_cbc.c bf_skey.c bf_module.c

# camellia
SRCS+=  camellia.c camellia-api.c

# cast128
SRCS+=	cast128.c

# DES
SRCS+=	des_ecb.c des_setkey.c des_enc.c des_cbc.c des_module.c

# rijndael
SRCS+=	rijndael-alg-fst.c rijndael-api-fst.c rijndael.c

# skipjack
SRCS+=	skipjack.c

.include <bsd.lib.mk>
.include <bsd.klinks.mk>
