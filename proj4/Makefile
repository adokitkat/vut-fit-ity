PROJ=proj4
LOGIN=xmudry01
BIB=bibliografia

.PHONY: clean pack pdflatex

all: pdflatex

pdflatex:
	pdflatex $(PROJ).tex
	bibtex $(PROJ)
	pdflatex $(PROJ).tex
	pdflatex $(PROJ).tex

pack: $(PROJ).tex Makefile
	tar -czf $(LOGIN)-fit.tar.gz Makefile $(PROJ).tex $(BIB).bib czechiso.bst

clean:
	rm -f $(PROJ).aux $(PROJ).log $(PROJ).out $(PROJ).dvi $(PROJ).ps $(PROJ).bbl $(PROJ).blg

clean-all:
	rm -f $(LOGIN)-fit.tar.gz $(PROJ).aux $(PROJ).log $(PROJ).out $(PROJ).dvi $(PROJ).ps $(PROJ).bbl $(PROJ).blg $(PROJ).pdf