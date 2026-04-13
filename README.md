# cookiecutter-latex-paper

A minimal Cookiecutter template for LaTeX papers.

## Usage

1. Install Cookiecutter if needed:

   ```bash
   pip install cookiecutter
   ```

2. Generate a new project from this template:

   ```bash
   cookiecutter path/to/cookiecutter-latex-paper
   ```

   You will be prompted for:

   - `project_name` (e.g. "My Cool Paper")
   - `project_slug` (e.g. "paper_XXXX")

3. Change into the generated project directory:

   ```bash
   cd paper_XXXX  # or whatever slug you chose
   ```

4. Build the paper:

   ```bash
   cd main
   make
   ```

   This runs `latexmk` on `src/main.tex` and writes `main.pdf` in `main/`.

## Layout

The generated project has the following structure:

- `main/`
  - `Makefile` — builds `src/main.tex` to `main.pdf`
  - `src/`
    - `main.tex` — minimal document skeleton
    - `config.tex` — shared packages and numbering conventions
    - `abstract.tex` — abstract shell
    - `intro.tex` — introduction shell
    - `fig/`
      - `src/` — raw figure data (empty, with .gitkeep)
      - `tikz/fig1.tex` — example TikZ figure shell
      - `caption/fig1.tex` — example caption shell
    - `sec/` — for additional sections (empty, with .gitkeep)
    - `supsec/` — for supplementary sections (empty, with .gitkeep)

You add your own content to the `.tex` files and create additional sections/figures as needed.
