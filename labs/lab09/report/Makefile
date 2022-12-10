FILES = $(patsubst %.md, %.docx, $(wildcard *.md))
FILES += $(patsubst %.md, %.pdf, $(wildcard *.md))

LATEX_FORMAT = 

FILTER = --filter pandoc-crossref

FILTERS =
OPTIONS =
PDF_ENGINE =
PDF_OPTIONS =
FORMAT_OPTIONS =


%.docx: %.md
	-pandoc "$<" $(FILTER) -o "$@"

%.pdf: %.md
	-pandoc "$<" $(LATEX_FORMAT) $(FILTER) -o "$@"

all: $(FILES)
	@echo $(FILES)


clean:
	-rm $(FILES) *~

cleanall: clean
