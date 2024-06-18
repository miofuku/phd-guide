SOURCES_DIR = sources
OUTPUT_DIR = pdfs

TEX_FILES := $(wildcard $(SOURCES_DIR)/*.tex)

PDF_FILES := $(patsubst $(SOURCES_DIR)/%.tex, $(OUTPUT_DIR)/%.pdf, $(TEX_FILES))

LATEX = pdflatex

all:	$(PDF_FILES)

# Rule to compile .tex files to .pdf
$(OUTPUT_DIR)/%.pdf:	$(SOURCES_DIR)/%.tex | $(OUTPUT_DIR)
	$(LATEX) -output-directory $(OUTPUT_DIR) $<
	
# Create the output directory if it doesn't exist
$(OUTPUT_DIR):
	mkdir -p $(OUTPUT_DIR)
	
# Clean up generated files
clean:
	rm -rf $(OUTPUT_DIR)

.PHONY: all clean


