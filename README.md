This is a TeXromancers retypesetting of J. C. Lagarias and A. M. Odlyzko, “Effective Versions of the Chebotarev Density Theorem,” in *Algebraic Number Fields* (Academic Press, 1977), pp. 409–464.

Published PDFs:
- [Standard version](https://aareyanmanzoor.github.io/assets/articles/lagarias-odlyzko.pdf)
- [Dyslexic-friendly version](https://aareyanmanzoor.github.io/assets/articles/lagarias-odlyzko-dyslexic.pdf)

## Corrections and editorial policy

The October 2026 corrections restore the trivial-zero coefficients and cutoffs, the placement of a zero-sum summand, contour endpoints and orientation, the convergent horizontal-integral bound, the double-angle identity and pole denominator, the Stark field tower, the quantified least-prime constants, norm weights and field degrees, the near-\(x\) variable, the zero-free-region comparison and absolute ordinate, and the defined zero-counting function. The recalled \(I_C(x,T)\) and \(L(s,\chi)\) arguments and Moreno’s title are also restored.

Intentional modernization, including \(\Delta_L\) for the absolute discriminant, is retained. Errors inherited from the original are corrected rather than silently reproduced, with editor’s footnotes in the article: the false uniform root-discriminant bound is replaced by the explicit positive bound \(\log(\Delta_L)/n_L\geq\log(\pi/2)\) for \(n_L>1\); Theorem 1.4 refers to the field \(L\), not “1”; the small-zero signs follow Lemma 5.5; equation (6.11) uses the lower-height denominator; the smoothing integrands use \(F_C(s)\); and the digamma variable, fixed horizontal height, and reflected contour endpoint are made consistent.

The Mellin reference now cites Titchmarsh rather than Tschebotareff; its page reference is updated to pp. 60–61 of the retained 1986 second edition, whose author/revision credits are corrected. The corresponding Davenport reference uses pp. 105–106 of the retained second-edition reprint, with Montgomery credited as reviser. All three Fogels installments are cited, so the bibliography retains every work represented by the original 17 grouped references. Their dates and the third installment’s volume/pages follow the authoritative EuDML records: [I](https://eudml.org/doc/207002), [II](https://eudml.org/doc/206994), and [III](https://eudml.org/doc/207003), all dated 1962, rather than the original’s inconsistent details. Moreno’s preprint is recorded as an unpublished work, not an article with an unspecified journal.

For the corrected discriminant bound, see [Sharifi, *Algebraic Number Theory*, Corollary 4.3.6](https://math.ucla.edu/~sharifi/notes/algnum-ch04.html#thm:lower_bound_discr_num_fld). Original-source comparisons use the [published proceedings scan](https://archive.org/download/albrecht-frohlich-algebraic-number-fields-l-functions-and-galois-properties-academic-press/%5BAlbrecht%20Fr%C3%B6hlich%5D%20Algebraic%20Number%20Fields_%20L-functions%20and%20Galois%20Properties%20%5BAcademic%20Press%5D.pdf); printed page \(p\) is PDF page \(p+9\).

## Building

Use a current TeX distribution with pdfLaTeX, `latexmk`, the packages listed in `preamble/packages.tex`, and a working Biber compatible with the installed `biblatex`. From the repository root:

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=build main.tex
```

The output is `build/main.pdf`. Biber is required: direct pdfLaTeX-only passes leave the citations unresolved and the bibliography empty. Allow `latexmk` to run Biber and all required subsequent LaTeX passes. Generated build products are not source files.
