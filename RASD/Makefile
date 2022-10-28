TARGET := document

TF := texfot
CC := latexmk

OUTDIR := ./out
LFLAGS := -bibtex -halt-on-error -file-line-error -synctex=1 -interaction=nonstopmode
SHESC := -shell-escape
DRAFT := -d
ENGINE := -lualatex

OPEN_COMMAND := open

main: $(OUTDIR)
	$(TF) $(CC) $(TARGET) -outdir=$(OUTDIR) $(ENGINE) $(LFALGS)

draft: $(OUTDIR)
	$(TF) $(CC) $(TARGET) -outdir=$(OUTDIR) $(ENGINE) $(DRAFT) $(LFALGS)

clean:
	@# @find ./out/ ! -name '*.pdf' -type f -exec rm -f {} +
	@$(CC) -outdir=$(OUTDIR) -c

open:
	@$(OPEN_COMMAND) $(OUTDIR)/$(TARGET).pdf

$(OUTDIR):
	@mkdir -p $(OUTDIR)
