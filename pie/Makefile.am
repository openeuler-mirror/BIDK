
noinst_LTLIBRARIES = libpie.la

libpie_la_SOURCES = \
	pie-a64-decoder.c \
	pie-a64-encoder.c \
	pie-a64-field-decoder.c

noinst_HEADERS = \
	LICENSE \
	a64.txt \
	arm.txt \
	generate_common.rb \
	generate_decoder.rb \
	generate_encoder.rb \
	generate_field-decoder.rb \
	pie-a64-decoder.h \
	pie-a64-encoder.h \
	pie-a64-field-decoder.h \
	riscv.txt \
	thumb.txt

libpie_la_CFLAGS = \
            $(BASE_CFLAGS) \
            $(OPT_CFLAGS) \
            -Wall

libpie_la_CPPFLAGS = $(BASE_CPPFLAGS)

libpie_la_LDFLAGS = -static

