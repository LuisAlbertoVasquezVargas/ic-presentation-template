# IC Presentation Template

A modular LaTeX Beamer template designed for technical presentations, specifically optimized for Computer Science and Scientific Redaction workflows.

## 🛠 Local Setup

This project is designed for a terminal-based LaTeX environment. It avoids dependencies on cloud editors to ensure full control over the build pipeline.

### Installation

To install the full set of dependencies on Arch Linux (or Omarchy), run:

```bash
sudo pacman -S texlive-basic texlive-latexextra texlive-fontsrecommended \
               texlive-fontsextra texlive-bibtexextra texlive-plaingeneric \
               texlive-binextra texlive-science biber zathura
```

### Build Instructions

The following command prepares the output directory, sets the search paths for TeX components, and launches `latexmk` in continuous preview mode with Zathura:

```bash
mkdir -p output && find output -type f -delete && \
trap 'pkill -P $$ zathura' EXIT; \
BIBINPUTS="./src/sections/:" \
BSTINPUTS="./src/sections/:" \
TEXINPUTS="./src//:./src/img//:" \
latexmk -pdf -pvc -e '$pdf_previewer="zathura %S"' -outdir=output src/main.tex
```

## 📂 Project Structure

The structure follows the convention of the Topicos (Scientific Redaction) report for seamless content porting:

```text
.
├── README.md               # Setup
└── src/
    ├── main.tex            # Main entry point
    ├── structure/
    │   ├── engine.tex      # LaTeX packages and Beamer configuration
    │   └── metadata.tex    # Presentation and author information
    └── sections/           # Modular slide files
        ├── 01_intro.tex
        ├── 02_methodology.tex
        └── 99_questions.tex
```

## 🚀 Last Working Code (LWC)

Use this command to generate a full project dump for LLM context. This command prunes hidden directories and non-source files, ensuring the model receives a clean representation of the current project state.

```bash
find . -path './.*' -prune -o -name "*.tex" -exec cat {} +
```
