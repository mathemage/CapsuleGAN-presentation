#texCompiler = xelatex
texCompiler = pdflatex
all: CapsuleGAN.pdf

# LaTeX must be run multiple times to get references right
CapsuleGAN.pdf: CapsuleGAN.tex $(wildcard *.tex) ../bibliography.bib
	${texCompiler} $<
	bibtex CapsuleGAN
	${texCompiler} $<
	${texCompiler} $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *._aux *._log *.nav *.synctex.gz *.project.vim *-blx.bib *.run.xml *.snm
	rm -rf .tmp/*
	rm -f CapsuleGAN.pdf
