# Mathematical Methods

Public project ID: `math-methods`. Public server root: `https://notes.rua.rs`.
The course folder name and public project ID serve different purposes.

Planned GitHub repository: `Redstone-D/mathematical-methods-notes`.

## Local template

- `notes-common.sty`: canonical shared Core, copied unchanged from `latex-course-repo`
- `notes-project.sty`: this course's public identity and package loading
- `rs-notes.sty`: shared personal authoring conventions
- `LATEX_AUTHORING_GUIDE.md`: semantic block and reference syntax
- `lec01.tex`, `tut01.tex`: empty lecture and tutorial starters
- `cheatsheet.tex`: empty compact-reference starter
- `.latexmkrc`, `.vscode/`: local build configuration
- `latex_target/manifest.json`: project metadata

```sh
latexmk -pdf lec01.tex
latexmk -pdf tut01.tex
latexmk -pdf cheatsheet.tex
```

Auxiliary files go into `.build/`; finished PDFs go into `latex_target/`.
The files above are starters; no new mathematical exposition has been written.

## Chapter roadmap

Each chapter uses the `lec01.tex` starter from the notes-server LaTeX template.
The chapter files currently contain only the document header and chapter title.

| Document | Title | Status |
|---|---|---|
| [ch01.tex](ch01.tex) | Complex Numbers and Euler's Formula | Title only |
| [ch02.tex](ch02.tex) | Multivariable Calculus | Title only |
| [ch03.tex](ch03.tex) | Vector Calculus | Title only |
| [ch04.tex](ch04.tex) | Ordinary Differential Equations | Title only |
| [ch05.tex](ch05.tex) | Laplace Transforms | Title only |
| [ch06.tex](ch06.tex) | Fourier Series and Transforms | Title only |
| [ch07.tex](ch07.tex) | Partial Differential Equations | Title only |
| [ch08.tex](ch08.tex) | Linear Algebra for Physics | Title only |
| [ch09.tex](ch09.tex) | Taylor Expansions and Approximation Methods | Title only |

For the immediate prerequisite work, start with `ch01.tex`, `ch04.tex`,
`ch08.tex`, and `ch09.tex`, adjusting the order to the exam topics. The first
seven chapter numbers preserve the earlier roadmap; linear algebra and Taylor
approximations are appended as chapters 8 and 9.

Use [START_PROMPT.txt](START_PROMPT.txt) to begin a new study session.

## Shared material and references

General calculus, ODE, and transform methods belong in `math-methods`. EM laws and applications belong in `em`; physical oscillations and waves belong in `waves`. Use existing analysis definitions when available, and mark missing foundations with `\missingprereq{concept, owning subject}`.

Use `\xref[descriptive text]{project::document::kind:id}` for a verified
cross-project target. Cheat sheets can repeat useful equations and link to
their full definitions or theorems. Keep reusable notation in a separate
subject package when it becomes necessary.


## Server registration files

`config.json` and `manifest.json` at this folder's root are local setup
copies excluded from Git. Copy both into the notes server's
`config/math-methods/` directory when registering this project.

The GitHub source URL is `https://github.com/Redstone-D/mathematical-methods-notes.git`.
Create that repository with this subject-based name.
The server's project ID remains `math-methods`.

`latex_target/manifest.json` is the separate public metadata file and stays
in the course repository. Preparing these JSON files does not register or
deploy the project.

## Publication

The local project has no remote repository or server registration yet.
The optional `.github/workflows/deploy.yml.template` is configured with this
project's ID and the `main` branch, and remains inactive as a template.
Register the project and repository separately before enabling deployment.
Only `latex_target/` is published by the notes server.
