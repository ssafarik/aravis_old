include $(top_srcdir)/Makefile.decl

INCLUDES = -g -I$(top_srcdir)/src/ $(ARAVIS_CFLAGS)

test_progs_ldadd = 					\
	$(top_builddir)/src/libaravis.la		\
	$(ARAVIS_LIBS)

noinst_PROGRAMS = arv-test arv-genicam-test arv-evaluator-test arv-zip-test arv-camera-test

arv_test_SOURCES = arvtest.c
arv_test_LDADD = $(test_progs_ldadd)

arv_genicam_test_SOURCES = arvgenicamtest.c
arv_genicam_test_LDADD = $(test_progs_ldadd)

arv_evaluator_test_SOURCES = arvevaluatortest.c
arv_evaluator_test_LDADD = $(test_progs_ldadd)

arv_zip_test_SOURCES = arvziptest.c
arv_zip_test_LDADD = $(test_progs_ldadd)

arv_camera_test_SOURCES = arvcameratest.c
arv_camera_test_LDADD = $(test_progs_ldadd)

TEST_PROGS += evaluator fake

noinst_PROGRAMS += $(TEST_PROGS)

evaluator_SOURCES = evaluator.c
evaluator_LDADD = $(test_progs_ldadd)

fake_SOURCES = fake.c
fake_CFLAGS = -DGENICAM_FILENAME="\"$(top_srcdir)/src/arv-fake-camera.xml\""
fake_LDADD = $(test_progs_ldadd)
