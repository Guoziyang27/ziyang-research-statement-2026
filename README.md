# template-research-statement

## RegLab application version (October 2026)

The RegLab cover letter is in `tex/reglab-cover-letter.tex`, with its entry point
in `cover-letter-reglab.tex`. It uses the statement's `researchstatement` class
and body font, with a Northwestern Computer Science letterhead adapted from
[Fumeng Yang's reference letter](https://www.fmyang.com/files/statements/GENERIC-letter_2023.pdf).
The vector wordmark in `pic/northwestern-cs-letterhead.pdf` was extracted from
that reference; the institutional address, recipient, date, and contact footer
are editable LaTeX in the entry-point file. The current revision fits on one page
with 11-point body text. Compile with XeLaTeX.
The compiled application PDF is
`output/pdf/ziyang-guo-reglab-cover-letter.pdf`. Compile from the repository root:

```sh
latexmk -xelatex cover-letter-reglab.tex
latexmk -xelatex template-RS.tex
```

The cover letter addresses the [RegLab posting](https://hai.stanford.edu/research/fellowship-programs#reglab)'s
research, methods, fit, and professional-goals requirements. The current draft
preserves the author's revised focus on creative tasks, tacit expertise, and
collaboration with agency partners. Expected PhD completion is 2027,
as listed in the [September 2026 CV](https://ziyangguo.com/assets/pdf/ziyang_guo_CV.pdf).

Verified updates also applied to the original statement and bibliography:

- [ComplLLM](https://www.hullmanlab.northwestern.edu/paper/2026/10/04/complllm.html)
  is accepted at NeurIPS 2026. Its bibliography entry now names the main-conference
  venue and uses Kenneth Holstein's full name.
- The [ICLR 2026 paper](https://www.hullmanlab.northwestern.edu/paper/2026/01/01/aciv.html)
  is now titled *Explaining and Improving Information Complementarities in
  Multi-Agent Decision-making*. Unverified volume and page fields were removed.
- Human-study wording now identifies the preregistered 421-participant house-price
  experiment from the [ICLR paper](https://ziyangguo.com/assets/pdf/ICLR2026_informative_analysis.pdf).
  The [public ComplLLM preprint](https://arxiv.org/html/2602.19458v1) supports the
  listed application domains but does not establish the original blanket claim
  of preregistered human improvements across those domains. The wording therefore
  distinguishes those evaluations from the verified human experiment.

## Original template documentation

![Preview](preview.png)

This is the format I created for my faculty job applications in the 2023--24 cycle. You can view my research statement at this [link](https://www.fmyang.com/files/statements/Fumeng_Yang-RS_2023.pdf). Several people asked me for this template. I'm happy to share it, although I think this template is a little hard to use. :-) It works best if you need lots of figures. The main file is `template-RS.tex`, and most of the formatting is in `researchstatement.cls`.

**2024/12/23 update**: This template is unexpectedly getting a bit of attention. I converted `format.tex` into a `.cls` file and also fixed the figure caption font problems.

**2026/01/09 update**: Getting a bit bored in Key Largo. I made minor changes to "Please read!" and font size, and used Cursor to standardize the `.cls` file.

## Basics

You need to use XeLaTeX to compile this document. On Overleaf, Menu → Compiler. You should change the name (First Last) in the `template-RS.tex` file.

The colors are specified in the `researchstatement.cls` file, around line 92. The convention is to match your home school color.

The figure on the right is specified using `minipage`. The drawback is that you have to end the text at the same position as the figure. If the text is too long, the text column will overflow and the whole page will be pushed to the next page. So you have to end the text at the right point, or move the extra part to the next page manually. Sometimes `\vspace` gives you a bit of extra room. Sorry, I don't know how to make this more flexible. You may need to use lots of `\vspace`. P.S. using `wrapfigure` will be more painful.

## Advanced

**Font** The fonts I used for my applications are slightly different. I changed them because one of them is a commercial font, and because I want to preserve a bit of uniqueness :-). I chose different fonts, but I also think these fonts are decent. You can change them by loading different TTF files in the `researchstatement.cls` file. I suggest using a font that matches your CV. So if you use a serif font in your CV, you should at least use a serif font here. I chose to use the identical fonts—Your materials will be reviewed together.

**Spacing and Size** You can change line spacing (`\linespread`, around line 185), section title size, page margin, paragraph spacing (`\parskip`) etc. in the `researchstatement.cls` file. You can change the font size in the main file.
