THISDIR := miscphysics
THISBOOK := $(THISDIR)

export BOOKSUBVER := 1
export BOOKMAJVER := 0
# This isn't a good way to version.  It depends on the local git reflog history count.
export REVCOUNTSTART := 1

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

include ../latex/make.rules

#figures/%.png: %.png
#	cp $< $@

backmatter.tex : ../latex/classicthesis_mine/backmatter.tex
	cp $< $@

#listings/%.pl: %.pl
#	mkdir -p $(@D)
#	cp $< $@

vpath %.png $(ORIG_FIGURE_DIRS)
vpath %.pl $(ORIG_LISTING_DIRS)
