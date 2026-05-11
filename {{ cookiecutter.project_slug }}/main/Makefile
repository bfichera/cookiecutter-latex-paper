.PHONY: main clean FORCE

SRC_DIR := src
OUTDIR := ..
AUXDIR := .build
LATEXMK := latexmk
PDFLATEX := lualatex -interaction nonstopmode

main: main.pdf

main.pdf: FORCE
	cd "$(SRC_DIR)" && \
	$(LATEXMK) -lualatex="$(PDFLATEX)" -output-directory="$(OUTDIR)" -aux-directory="$(AUXDIR)" -pdf main.tex

clean:
	cd "$(SRC_DIR)" && \
	$(LATEXMK) -output-directory="$(OUTDIR)" -aux-directory="$(AUXDIR)" -c -pdf main.tex
