# Makefile for jobcomp/kafka plugin

AUTOMAKE_OPTIONS = foreign

PLUGIN_FLAGS = -module -avoid-version --export-dynamic

AM_CPPFLAGS = -I$(top_srcdir) -I$(top_srcdir)/src/common $(LIBCURL_CPPFLAGS)

AS_KAKFKA_SOURCES = jobcomp_kafka.c

if WITH_CURL
pkglib_LTLIBRARIES = jobcomp_kafka.la

jobcomp_kafka_la_SOURCES = $(AS_KAFKA_SOURCES)
jobcomp_kafka_la_LDFLAGS = $(PLUGIN_FLAGS)
jobcomp_kafka_la_LIBADD = $(LIBCURL)

else
EXTRA_jobcomp_kafka_la_SOURCES = $(AS_KAFKA_SOURCES)
endif
