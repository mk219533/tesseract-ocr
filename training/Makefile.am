SUBDIRS =
AM_CPPFLAGS = \
    -I$(top_srcdir)/ccutil -I$(top_srcdir)/ccstruct \
    -I$(top_srcdir)/image -I$(top_srcdir)/viewer \
    -I$(top_srcdir)/ccops -I$(top_srcdir)/dict \
    -I$(top_srcdir)/classify -I$(top_srcdir)/display \
    -I$(top_srcdir)/wordrec -I$(top_srcdir)/cutil \
    -I$(top_srcdir)/textord

EXTRA_DIST = unicharset_extractor.vcproj wordlist2dawg.vcproj \
    cntraining.vcproj mftraining.vcproj

include_HEADERS = \
    commontraining.h mergenf.h name2char.h

lib_LIBRARIES = libtesseract_training.a
libtesseract_training_a_SOURCES = \
    name2char.cpp commontraining.cpp

bin_PROGRAMS = cntraining combine_tessdata mftraining unicharset_extractor wordlist2dawg
combine_tessdata_SOURCES = combine_tessdata.cpp
combine_tessdata_LDADD = \
    ../ccutil/libtesseract_ccutil.a

cntraining_SOURCES = cntraining.cpp
cntraining_LDADD = \
    libtesseract_training.a \
    ../textord/libtesseract_textord.a \
    ../classify/libtesseract_classify.a \
    ../dict/libtesseract_dict.a \
    ../ccstruct/libtesseract_ccstruct.a \
    ../image/libtesseract_image.a \
    ../cutil/libtesseract_cutil.a \
    ../viewer/libtesseract_viewer.a \
    ../ccutil/libtesseract_ccutil.a

mftraining_SOURCES = mftraining.cpp mergenf.cpp
mftraining_LDADD = \
    libtesseract_training.a \
    ../textord/libtesseract_textord.a \
    ../classify/libtesseract_classify.a \
    ../dict/libtesseract_dict.a \
    ../ccstruct/libtesseract_ccstruct.a \
    ../image/libtesseract_image.a \
    ../cutil/libtesseract_cutil.a \
    ../viewer/libtesseract_viewer.a \
    ../ccutil/libtesseract_ccutil.a

unicharset_extractor_SOURCES = unicharset_extractor.cpp
unicharset_extractor_LDADD = \
    ../ccutil/libtesseract_ccutil.a

wordlist2dawg_SOURCES = wordlist2dawg.cpp
wordlist2dawg_LDADD = \
    ../classify/libtesseract_classify.a \
    ../dict/libtesseract_dict.a \
    ../ccstruct/libtesseract_ccstruct.a \
    ../image/libtesseract_image.a \
    ../cutil/libtesseract_cutil.a \
    ../viewer/libtesseract_viewer.a \
    ../ccutil/libtesseract_ccutil.a
