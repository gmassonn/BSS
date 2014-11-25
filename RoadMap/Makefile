all: RoadMap.pdf

RoadMap.pdf: RoadMap.dvi
	dvips RoadMap.dvi
	ps2pdf RoadMap.ps

RoadMap.dvi: RoadMap.aux VSS.bib
	bibtex RoadMap.aux
	latex --shell-escape RoadMap.tex
	latex --shell-escape RoadMap.tex

RoadMap.aux: RoadMap.tex Introduction.tex Modularity.tex Analysis.tex	
	latex --shell-escape RoadMap.tex

clean:
	rm *.pdf *.ps *.dvi *.aux *.bbl *.blg *.log
