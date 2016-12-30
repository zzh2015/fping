AM_CFLAGS = -Wall -Wextra -Wno-sign-compare

prog =

if IPV4
prog += fping
endif
if IPV6
prog += fping6
endif

sbin_PROGRAMS = ${prog}

fping_SOURCES = fping.c seqmap.c socket.c socket4.c cJSON.c fping.h options.h seqmap.h cJSON.h
fping_LDADD = -lm
fping_DEPENDENCIES = ../config.h
fping6_SOURCES = fping.c seqmap.c socket.c socket6.c cJSON.c fping.h options.h seqmap.h cJSON.h
fping6_LDADD = -lm
fping6_DEPENDENCIES = ../config.h
fping6_CFLAGS = $(AM_CFLAGS) -DIPV6
