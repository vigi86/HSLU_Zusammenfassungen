# aux: auxiliary
# toc: table of content
# lof: list of figurs
# lot: list of tables
# bib: bibtex (sources)

# replace MAINTEX with the root tex file.

#all: NETT_HS21.pdf clean
all: NETT_HS21.pdf

clean:
	rm -f *.acn *.acr *.alg *.aux *.bbl *.bcf *.blg *.fdb_latexmk *.fls *.glg *.glo *.gls *.idx *.ilg *.ind *.ist *.lof *.log *.lot *.out *.run.xml *.toc

#NETT_HS21.pdf: *.tex *.ilg *.glo *.bib go
NETT_HS21.pdf: *.tex *.ilg *.glo go
	pdflatex NETT_HS21 && pdflatex NETT_HS21

NETT_HS21.tex: go
	pdflatex NETT_HS21

*.ilg: go
	makeindex NETT_HS21

*.glo: go
	makeglossaries NETT_HS21

*.bib: go
	biber NETT_HS21

.PHONY: all clean go