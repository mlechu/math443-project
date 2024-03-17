JUNK = main.aux main.fdb_latexmk main.fls main.log main.out main.blg main.bbl main.nav main.snm main.toc
OUT = main.pdf

# $(OUT) means it will recompile everything every time
# being cautious around latexmk, but might not be necessary
.PHONY: all clean $(OUT)

all: $(OUT)

clean:
	rm $(JUNK)
	rm $(OUT)

main.pdf: main.tex citations.bib
	latexmk -pdf -bibtex
	rm $(JUNK)
