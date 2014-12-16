
#AM_CFLAGS = -g -std=c99 -D_GNU_SOURCE -Wstrict-aliasing=0 -O3 -pthread -I../deps/inih/ -I../deps/libev/
AM_CFLAGS = -g -std=c99 -D_GNU_SOURCE -Wstrict-aliasing=0 -O3 -pthread -I../deps/libev/

#LIBS = -lm -lev -lpthread -lrt
LIBS = -lm -lpthread -lev -lrt

EXTRA_DIST = ../deps/libev/*

bin_PROGRAMS = statsite

statsite_SOURCES = hashmap.c hashmap.h heap.c heap.h radix.c radix.h hll_constants.c hll_constants.h hll.c hll.h set.c set.h cm_quantile.c cm_quantile.h timer.c timer.h counter.c counter.h metrics.c metrics.h streaming.c streaming.h config.c config.h networking.c networking.h conn_handler.c conn_handler.h statsite.c MurmurHash3.c MurmurHash3.h ini.c ini.h 

