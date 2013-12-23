FILE = ms
REF = references
TEX = latex
BIBTEX = bibtex
DVIPDF = dvipdf

.PHONY: all clean

all: $(FILE).dvi $(FILE).pdf

#$(FILE).dvi : $(FILE).tex $(REF).bib makefile
$(FILE).dvi : $(FILE).tex references.tex makefile 
	$(TEX) $(FILE)
#	$(BIBTEX) $(FILE)
	$(TEX) $(FILE)
	$(TEX) $(FILE)

$(FILE).pdf : $(FILE).dvi
	$(DVIPDF) $(FILE).dvi
#	open $(FILE).pdf &

clean :
	\rm *.aux
	\rm *.log
	\rm *.dvi
	\rm *.out
	\rm *Notes.bib
#	\rm *.bbl	
#	\rm *.blg	
