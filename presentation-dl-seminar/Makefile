all: CapsNet.pdf

# LaTeX must be run multiple times to get references right
CapsNet.pdf: CapsNet.tex $(wildcard *.tex) ../bibliography.bib
	xelatex $<
	bibtex CapsNet
	xelatex $<
	xelatex $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *._aux *._log *.nav *.synctex.gz *.project.vim *-blx.bib *.run.xml *.snm
	rm -rf .tmp/*
	rm -f CapsNet.pdf
