# Curriculum vitae

<p align=center>
<a href="">
<img alt="screenshot" src="https://user-images.githubusercontent.com/18266391/87251999-11121380-c470-11ea-9098-492129351480.png">
</a>
</p>
<p align=center>
    <a><img alt="LaTeX" src="https://img.shields.io/badge/Built_with-LaTeX-blue.svg"></a>
    <a><img alt="Package" src="https://img.shields.io/badge/package-moderncv-orange.svg"></a>
    <a><img alt="Font" src="https://img.shields.io/badge/Font-Source Sans Pro-lightgray.svg"></a>
</p>

Resume built using LaTeX and moderncv.
> [`witekbobrowski-cv.pdf`](builds/witekbobrowski-cv.pdf)

## Contents

```
.
├── LICENSE
├── README.md
├── builds
│   └── witekbobrowski-cv.pdf
├── sections
│   ├── education.tex
│   ├── experience.tex
│   ├── languages.tex
│   ├── scholarships.tex
│   └── skills.tex
└── witekbobrowski-cv.tex
```

Very simple structure so only few things worth explaining here:

- [`witekbobrowski-cv.tex`](witekbobrowski-cv.tex) is the main file that defines document structure and links other tex files from sections directory.

- [`sections`](sections/) directory contains other tex files that are separating CV content into smaller modules making it more readable.

- [`builds`](builds/) directory is here to not have top directory cluttered with build output

- [`witekbobrowski-cv.pdf`](builds/witekbobrowski-cv.pdf) is the most recent build of the document. It's also the reason you are here.

## Usage

### Dependencies

If you really want to build it from source, make sure to have following dependencies installed:

- [LaTeX](https://www.latex-project.org/get/) distribution appropriate for your platform.

- [moderncv](https://www.ctan.org/pkg/moderncv) package that makes this document look fancy.

- [Source Sans Pro](https://github.com/adobe-fonts/source-sans-pro) font to make it even prettier.

- [lualatex](http://luatex.org/download.html) compilation tool of choice, feel free to use different one (you may encounter some errors).

### Building

#### Simple

To compile the document using lualatex run:

```
$ lualatex witekbobrowski-cv.tex
```

#### Customised

What I like to do is to supply lualatex with these extra options for customised behaviour:

- `--output-directory=builds` makes the output land in the builds directory.

- `--output-format=pdf` not really needed but makes it explicit for lualatex to produce PDF file.

- `--interaction=batchmode` stops lualatex from printing houndreds of lines into the terminal.

```
$ lualatex --output-directory=builds --output-format=pdf --interaction=batchmode witekbobrowski-cv.tex
```

The output is where it should be, and compilation message is short and sweet:

```
This is LuaTeX, Version 1.0.4 (TeX Live 2017)
 restricted system commands enabled.

luaotfload | main : initialization completed in 0.134 seconds%
```
