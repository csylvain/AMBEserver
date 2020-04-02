
sbin_PROGRAMS = AMBEserver

AMBEserver_SOURCES = ThumbDV/AMBEserver.c

init_ddir = /etc/init.d
dist_init_d_SCRIPTS = ThumbDV/init.d/AMBEserver

if WITH_GPIO
sbin_PROGRAMS += dv3000d

dv3000d_SOURCES = ThumbDV/dv3000d.c
dv3000d_LDADD = -lwiringPi
dv3000d_CPPFLAGS = -DRASPBERRY_PI
endif

