PROJ=proj3
LOGIN=xmudry01

.PHONY: clean pack pdflatex

all: pdf

pdf: $(PROJ).tex
	latex $(PROJ).tex
	latex $(PROJ).tex
	dvips -t a4 $(PROJ).dvi
	ps2pdf -sPAPERSIZE=a4 $(PROJ).ps

pack: $(PROJ).tex Makefile
	tar -czf $(LOGIN)-fit.tar.gz Makefile $(PROJ).tex oniisan.eps oniisan2.eps etiopan.eps algorithm2e.sty

clean:
	rm -f $(PROJ).aux $(PROJ).log $(PROJ).out $(PROJ).dvi $(PROJ).ps

clean-all:
	rm -f $(LOGIN)-fit.tar.gz $(PROJ).aux $(PROJ).log $(PROJ).out $(PROJ).dvi $(PROJ).ps $(PROJ).pdf