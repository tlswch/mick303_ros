DOCUMENT=main

$(DOCUMENT).pdf : $(DOCUMENT).tex
	latexmk -pdflatex="lualatex --halt-on-error --shell-escape %O %S" -pdf -dvi- -ps- "$<"

.PHONY : minted
minted : minted.sty
minted.sty :
	wget https://raw.githubusercontent.com/gpoore/minted/5219a9c8db6d8b9c1e7c3aeab892ab0f6fc74308/source/minted.sty

.PHONY : clean
clean :
	rm -rf $(DOCUMENT).aux $(DOCUMENT).log $(DOCUMENT).pdf $(DOCUMENT).out $(DOCUMENT).fls $(DOCUMENT).listing $(DOCUMENT).fdb_latexmk texput.log _minted-$(DOCUMENT) svg-inkscape
