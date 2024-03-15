JUNK = main.aux main.bbl main.blg main.dvi main.fdb_latexmk main.fls main.log
OUT = main.pdf

# $(OUT) means it will recompile everything every time
# being cautious around latexmk, but might not be necessary
.PHONY: all clean $(OUT)

all: $(OUT)

clean:
	rm $(JUNK)
	rm $(OUT)

main.pdf: main.tex citations.bib
	latexmk -bibtex
	rm $(JUNK)
