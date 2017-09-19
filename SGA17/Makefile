# make -f Makefile_latex

R = paper
STY = *.cls

pdf: $(R).pdf

$(R).bbl: $(R).bib
	pdflatex $(R)
	bibtex $(R)
	pdflatex $(R)

$(R).pdf:  *.tex $(STY) $(FIG) $(R).bbl
	pdflatex $(R)

clean:
	rm -f $(R).log $(R).aux $(R).bbl $(R).blg $(R).dvi $(R).ps $(R).out
