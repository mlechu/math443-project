JUNK = *.aux *.fdb_latexmk *.fls *.log *.out *.blg *.bbl *.nav *.snm *.toc
OUT = main.pdf

# $(OUT) means it will recompile everything every time
# being cautious around latexmk, but might not be necessary
.PHONY: all clean $(OUT)

all: $(OUT)

clean:
	rm $(JUNK)
	rm $(OUT)

main.pdf: main.tex
	latexmk -pdf -bibtex -interaction=nonstopmode main.tex
	rm $(JUNK) || true
