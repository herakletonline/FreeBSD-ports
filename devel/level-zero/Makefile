# $FreeBSD$

PORTNAME=	level-zero
DISTVERSIONPREFIX=	v
DISTVERSION=	0.91.10
CATEGORIES=	devel

PATCH_SITES=	https://github.com/${GH_ACCOUNT}/${GH_PROJECT}/commit/
PATCHFILES+=	4a42aa94cad2.patch:-p1 # https://github.com/oneapi-src/level-zero/pull/9

MAINTAINER=	jbeich@FreeBSD.org
COMMENT=	oneAPI Level Zero Specification Headers and Loader

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	${LOCALBASE}/include/CL/cl.h:devel/opencl

USES=		cmake compiler:c++14-lang
USE_GITHUB=	yes
USE_LDCONFIG=	yes
GH_ACCOUNT=	oneapi-src

post-extract:
	@${ECHO_CMD} ${DISTVERSION:E} >${WRKSRC}/VERSION_PATCH

.include <bsd.port.mk>
