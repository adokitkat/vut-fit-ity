PROJ=proj2
LOGIN=xmudry01

.PHONY: clean pack pdflatex

all: pdflatex

pdflatex: $(PROJ).tex
	pdflatex $(PROJ).tex
	pdflatex $(PROJ).tex

pack: $(PROJ).tex Makefile
	tar -czf $(LOGIN)-fit.tar.gz Makefile $(PROJ).tex

clean:
	rm -f $(PROJ).aux $(PROJ).log $(PROJ).out

clean-all:
	rm -f $(LOGIN)-fit.tar.gz $(PROJ).aux $(PROJ).log $(PROJ).out $(PROJ).pdf