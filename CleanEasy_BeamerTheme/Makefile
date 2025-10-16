# Makefile for CleanEasy Beamer Presentation

# Main TeX file (without extension)
MAIN = CleanEasy

# Compiler
LATEX = xelatex
LATEXFLAGS = -interaction=nonstopmode -halt-on-error

# Output PDF
PDF = $(MAIN).pdf

# Auxiliary files to clean
AUX_FILES = *.aux *.log *.nav *.out *.snm *.toc *.vrb *.bbl *.blg *.fls *.fdb_latexmk *.synctex.gz

.PHONY: all clean cleanall view help

# Default target
all: $(PDF)

# Build PDF (run twice for cross-references)
$(PDF): $(MAIN).tex
	@echo "Compiling $(MAIN).tex (first pass)..."
	@$(LATEX) $(LATEXFLAGS) $(MAIN).tex
	@echo "Compiling $(MAIN).tex (second pass)..."
	@$(LATEX) $(LATEXFLAGS) $(MAIN).tex
	@echo "Build complete: $(PDF)"

# Quick build (single pass)
quick: $(MAIN).tex
	@echo "Quick compiling $(MAIN).tex..."
	@$(LATEX) $(LATEXFLAGS) $(MAIN).tex

# Clean auxiliary files
clean:
	@echo "Cleaning auxiliary files..."
	@rm -f $(AUX_FILES)
	@echo "Clean complete."

# Clean everything including PDF
cleanall: clean
	@echo "Removing PDF..."
	@rm -f $(PDF)
	@echo "Deep clean complete."

# View PDF (macOS)
view: $(PDF)
	@echo "Opening $(PDF)..."
	@open $(PDF)

# Rebuild from scratch
rebuild: cleanall all

# Help message
help:
	@echo "CleanEasy Beamer Makefile"
	@echo "========================="
	@echo ""
	@echo "Available targets:"
	@echo "  make          - Build PDF (default, runs pdflatex twice)"
	@echo "  make quick    - Quick build (single pdflatex run)"
	@echo "  make clean    - Remove auxiliary files"
	@echo "  make cleanall - Remove all generated files including PDF"
	@echo "  make view     - Open the PDF with default viewer"
	@echo "  make rebuild  - Clean and rebuild from scratch"
	@echo "  make help     - Show this help message"
