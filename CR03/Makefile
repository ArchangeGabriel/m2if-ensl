IPEFIG=$(wildcard figures/*.ipe)
PDFFIG=$(IPEFIG:.ipe=.pdf)

all: notes.pdf

notes.pdf: *.tex $(PDFFIG)
	pdflatex notes.tex

%.pdf: %.ipe
	ipetoipe -pdf -export $<

clean:
	rm *.aux *.log figures/*.pdf notes.pdf
