AUTOMAKE_OPTIONS = foreign

AM_CPPFLAGS = \
  -I$(includedir) \
  -I$(OFFLINE_MAIN)/include \
  -isystem$(ROOTSYS)/include \
  -I$(OPT_SPHENIX)/include

AM_LDFLAGS = \
  -L$(libdir) \
  -L$(OFFLINE_MAIN)/lib

pkginclude_HEADERS = \
  Fun4AllEventOutStream.h \
  Fun4AllEventOutputManager.h \
  Fun4AllFileOutStream.h \
  Fun4AllPrdfInputManager.h \
  Fun4AllPrdfInputPoolManager.h \
  Fun4AllPrdfInputTriggerManager.h \
  Fun4AllPrdfOutputManager.h \
  Fun4AllRolloverFileOutStream.h \
  Fun4AllStreamingInputManager.h \
  InputManagerType.h \
  SingleGl1PoolInput.h \
  SingleGl1TriggerInput.h \
  SingleMbdTriggerInput.h \
  SingleInttPoolInput.h \
  SingleMicromegasPoolInput.h \
  SingleMvtxPoolInput.h \
  SinglePrdfInput.h \
  SingleStreamingInput.h \
  SingleTpcPoolInput.h \
  SingleTriggerInput.h \
  SingleZdcInput.h

lib_LTLIBRARIES = \
  libfun4allraw.la

libfun4allraw_la_SOURCES = \
  Fun4AllEventOutStream.cc \
  Fun4AllEventOutputManager.cc \
  Fun4AllFileOutStream.cc \
  Fun4AllPrdfInputManager.cc \
  Fun4AllPrdfInputPoolManager.cc \
  Fun4AllPrdfInputTriggerManager.cc \
  Fun4AllPrdfOutputManager.cc \
  Fun4AllRolloverFileOutStream.cc \
  Fun4AllStreamingInputManager.cc \
  intt_pool.cc \
  tpc_pool.cc \
  SingleGl1PoolInput.cc \
  SingleGl1TriggerInput.cc \
  SingleInttPoolInput.cc \
  SingleMbdTriggerInput.cc \
  SingleMicromegasPoolInput.cc \
  SingleMvtxPoolInput.cc \
  SinglePrdfInput.cc \
  SingleStreamingInput.cc \
  SingleTpcPoolInput.cc \
  SingleTriggerInput.cc \
  SingleZdcInput.cc

libfun4allraw_la_LIBADD = \
  -lffarawobjects \
  -lfun4all \
  -lEvent \
  -lphoolraw

BUILT_SOURCES = testexternals.cc

noinst_PROGRAMS = \
  testexternals

testexternals_SOURCES = testexternals.cc
testexternals_LDADD   = libfun4allraw.la

testexternals.cc:
	echo "//*** this is a generated file. Do not commit, do not edit" > $@
	echo "int main()" >> $@
	echo "{" >> $@
	echo "  return 0;" >> $@
	echo "}" >> $@

clean-local:
	rm -f $(BUILT_SOURCES)
