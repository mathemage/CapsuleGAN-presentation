all: AlphaZero.pdf

# LaTeX must be run multiple times to get references right
AlphaZero.pdf: AlphaZero.tex $(wildcard *.tex) ../bibliography.bib
	xelatex $<
	bibtex AlphaZero
	xelatex $<
	xelatex $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *._aux *._log *.nav *.synctex.gz *.project.vim *-blx.bib *.run.xml *.snm
	rm -rf .tmp/*
	rm -f AlphaZero.pdf
