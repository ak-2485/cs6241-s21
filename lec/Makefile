TEXINPUTS:=.

LEC= \
	pdf/background.pdf \
	pdf/2021-02-09.pdf \
	pdf/2021-02-11.pdf \
	pdf/2021-02-16.pdf \
	pdf/2021-02-18.pdf \
	pdf/2021-02-23.pdf \
	pdf/2021-03-02.pdf \
	pdf/2021-03-04.pdf \
	pdf/2021-03-11.pdf \
	pdf/2021-03-16.pdf \
	pdf/2021-03-23.pdf \
	pdf/2021-03-25.pdf \
	pdf/2021-03-30.pdf \
	pdf/2021-04-01.pdf \
	pdf/2021-04-06.pdf \
	pdf/2021-04-08.pdf \
	pdf/2021-04-13.pdf \
	pdf/2021-04-20.pdf \
	pdf/2021-04-22.pdf \
	pdf/2021-04-27.pdf \
	pdf/2021-04-29.pdf 

.PHONY: all copy
all: $(LEC)

pdf/%.pdf: notes/%.tex common.tex
	xelatex -output-dir pdf $<
	xelatex -output-dir pdf $<

clean:
	rm -f pdf/*.aux pdf/*.log pdf/*.out
	rm -f pdf/*.nav pdf/*.snm pdf/*.toc 
	rm -f pdf/*.vrb

distclean: clean
	rm -f pdf/*.pdf

copy:
	mkdir -p ../web/lec
	cp $(LEC) ../web/lec
