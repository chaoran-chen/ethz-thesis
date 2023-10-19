# ethz-thesis

LaTeX template for a PhD thesis at ETH Zurich.

## Changelog

- Based on [ClassicThesis](https://www.ctan.org/tex-archive/macros/latex/contrib/classicthesis/)
  by André Miede.
- Some ideas from [Patrick Pletscher](https://github.com/ppletscher/phd-thesis-sample)
  (title page, chapter folders).
- Adapted to A5 paperback size by [Tino Wagner (tuxu)](https://github.com/tuxu/ethz-thesis)
- June 2023: Updated dependencies
- June 2023: Introduced a bibliography section per chapter


## Usage

### Overleaf

This was tested with [Overleaf](https://www.overleaf.com/) in October 2023. The logs revealed 0 errors and 9 warnings (which is pretty good for LaTeX?).

### Local compilation

It is unknown when this was last tested and whether it still works.

- Install [TeXLive](https://www.tug.org/texlive/) or [MacTeX](http://www.tug.org/mactex/).
- Clone this repository.
- Run `make` from the top level directory to compile.
- …


## Cover

See [`cover/README.md`](cover/README.md) for instructions on how to create a soft cover.


## Sample PDF

[Sample](sample.pdf)

See my PhD thesis for a complete example:
[Science in Real-Time – Genomic Epidemiology During the SARS-CoV-2 Pandemic](https://www.research-collection.ethz.ch/handle/20.500.11850/637391).


## BibTeX cleaning

I used [bibtex-tidy](https://github.com/FlamingTempura/bibtex-tidy) to clean and format the BibTeX files. Specifically, I used the following setting:

```
bibtex-tidy \
  --omit=month,abstract,keywords,groups,file,editor,eprint,publisher,note,day,urldate,copyright,language,elocation-id \
  --curly \
  --numeric \
  --align=13 \
  --blank-lines \
  --duplicates=key \
  --no-escape \
  --sort-fields=title,shorttitle,author,year,month,day,journal,booktitle,location,on,publisher,address,series,volume,number,pages,isbn,issn,urldate,copyright,category,note,metadata,doi,url \
  --trailing-commas \
  --no-remove-dupe-fields \
  YOUR_FILE.bib
```


# License

[GPLv2](https://opensource.org/licenses/GPL-2.0) inherited from
[ClassicThesis](https://www.ctan.org/tex-archive/macros/latex/contrib/classicthesis/).
