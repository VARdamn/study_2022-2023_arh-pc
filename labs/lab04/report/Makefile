FILES = $(patsubst %.md, %.docx, $(wildcard *.md))
FILES += $(patsubst %.md, %.pdf, $(wildcard *.md))

LATEX_FORMAT = 

FILTER = --filter pandoc-crossref

FILTERS =
OPTIONS =
PDF_ENGINE =
PDF_OPTIONS =
FORMAT_OPTIONS =

FILTERS += -F pandoc-crossref
PDF_ENGINE += --pdf-engine=lualatex --pdf-engine-opt=--shell-escape
OPTIONS += --number-sections
BIB_OPTIONS = --citeproc


%.docx: %.md
	-pandoc "$<" $(FILTER) -o "$@"

%.pdf: %.md
	-pandoc "$<" $(LATEX_FORMAT) $(FILTER) -o "$@"

all: $(FILES)
	@echo $(FILES)


clean:
	-rm $(FILES) *~

cleanall: clean
