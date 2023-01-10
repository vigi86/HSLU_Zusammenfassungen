# aux: auxiliary
# toc: table of content
# lof: list of figurs
# lot: list of tables
# bib: bibtex (sources)

# replace MAINTEX with the root tex file.

#all: IBIS_FS22.pdf clean
all: IBIS_FS22.pdf

clean:
	rm -f *.acn *.acr *.alg *.aux *.bbl *.bib.bak *.bcf *.blg *.fdb_latexmk *.fls *.glg *.glo *.gls *.idx *.ilg *.ind *.ist *.lof *.log *.lot *.out *.run.xml *.toc

#IBIS_FS22.pdf: *.tex *.ilg *.glo *.bib go
IBIS_FS22.pdf: *.tex *.ilg go
	pdflatex IBIS_FS22 && pdflatex IBIS_FS22

IBIS_FS22.tex: go
	pdflatex IBIS_FS22

*.ilg: go
	makeindex IBIS_FS22

*.glo: go
	makeglossaries IBIS_FS22

*.bib: go
	biber IBIS_FS22

.PHONY: all clean go