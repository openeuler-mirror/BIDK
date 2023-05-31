
SUBDIRS=pie

noinst_LTLIBRARIES = libmambo.la

libmambo_la_SOURCES = \
    common.c \
    dbm.c \
    traces.c \
    syscalls.c \
    dispatcher.c \
    signals.c \
    util.S \
    api/helpers.c \
    api/plugin_support.c \
    api/branch_decoder_support.c \
    api/load_store.c \
    api/internal.c \
    api/hash_table.c \
    elf/elf_loader.c \
    elf/symbol_parser.c \
    arch/aarch64/dispatcher_aarch64_asm.S \
    arch/aarch64/dispatcher_aarch64.c \
    arch/aarch64/scanner_a64.c \
    api/emit_a64.c

noinst_HEADERS = \
	plugins.h \
	scanner_common.h \
	common.h \
	syscalls.h \
	dbm.h \
	kernel_sigaction.h \
	elf/elf_loader.h \
	util.h \
	scanner_public.h \
	api/emit_a64.h \
	api/helpers.h \
	api/hash_table.h \
	api/plugin_support.h \
	README.md \
	LICENSE

libmambo_la_CFLAGS = \
            $(BASE_CFLAGS) \
            $(OPT_CFLAGS) \
            -DDBM_LINK_UNCOND_IMM \
            -DDBM_INLINE_UNCOND_IMM \
            -DDBM_LINK_COND_IMM \
            -DDBM_LINK_CBZ \
            -DDBM_LINK_TBZ \
            -DDBM_TB_DIRECT \
            -DLINK_BX_ALT \
            -DDBM_INLINE_HASH \
            -DDBM_TRACES \
            -DPLUGINS_NEW \
            -D_GNU_SOURCE \
            -std=gnu99 \
            -Wunused-variable \
            -I/usr/include/libelf

libmambo_la_CPPFLAGS = $(BASE_CPPFLAGS)

libmambo_la_LDFLAGS = -static -Wl,-Ttext-segment=0x7000000000
libmambo_la_LIBADD = pie/libpie.la -lelf
