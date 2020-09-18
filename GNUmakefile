THISDIR := miscphysics
THISBOOK := $(THISDIR)

include make.revision
include ../latex/make.bookvars

FIGURES := ../figures/$(THISBOOK)

SOURCE_DIRS += $(FIGURES)
SOURCE_DIRS += algebra
SOURCE_DIRS += calculus
SOURCE_DIRS += cross
SOURCE_DIRS += electrodynamics
SOURCE_DIRS += feynman
SOURCE_DIRS += fletcher
SOURCE_DIRS += fourier
SOURCE_DIRS += maxwell
SOURCE_DIRS += probability
SOURCE_DIRS += qm
SOURCE_DIRS += relativity
SOURCE_DIRS += sort

#LOCAL_FIGURE_FILES += pendulumDouble.png
#ORIG_FIGURE_DIRS += ../gabook/figures
#ORIG_FIGURE_DIRS += ../phy354/figures/

GENERATED_SOURCES += cronology.tex
GENERATED_SOURCES += backmatter.tex

#ONCEFLAGS := -justonce
DO_SPELL_CHECK := $(shell cat spellcheckem.txt)

include ../latex/make.rules

.PHONY: spellcheck
spellcheck: $(patsubst %.tex,%.sp,$(filter-out $(DONT_SPELL_CHECK),$(DO_SPELL_CHECK)))

%.sp : %.tex
	spellcheck $^
	touch $@

#figures/%.png: %.png
#	cp $< $@

backmatter.tex : ../latex/classicthesis_mine/backmatter.tex
	cp $< $@

#listings/%.pl: %.pl
#	mkdir -p $(@D)
#	cp $< $@

vpath %.png $(ORIG_FIGURE_DIRS)
vpath %.pl $(ORIG_LISTING_DIRS)
