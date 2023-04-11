all: assignment3.pdf final.pdf

%.pdf: %.tex
	pdflatex $<
	pdflatex $<
	pdflatex $<
	- bash -c " ( grep Rerun $*.log && pdflatex $< ) || echo noRerun "
	- bash -c " ( grep Rerun $*.log && pdflatex $< ) || echo noRerun "

.PHONY: clean

clean:
	$(RM) *.log *.aux *.dvi *.out *.bib
	$(RM) *~

spotless: clean
	$(RM) assignment3.pdf
	$(RM) final.pdf
