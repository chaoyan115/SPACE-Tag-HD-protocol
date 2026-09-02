# SPACE-Tag-HD Protocol

Spatial CUT&Tag chromatin profiling adapted to the 10x Genomics Visium-HD platform.

Antibody-guided protein A-Tn5 tagmentation generates transcribable DNA fragments at target chromatin
loci. These are amplified by in vitro transcription and transferred to a Visium HD Slide on the
Visium CytAssist instrument, where they are captured on 2 µm barcoded squares.

**Read the protocol:** [protocol.md](protocol.md). A print-ready Word version is
[SPACE-Tag-HD-protocol.docx](SPACE-Tag-HD-protocol.docx), and [index.html](index.html) is the
rendered page.

> This repository is private while the manuscript is in revision. `index.html` is built and
> committed on every update, so turning on GitHub Pages (Settings → Pages → Deploy from a branch →
> `main` → `/ (root)`) publishes the site immediately, at
> `https://chaoyan115.github.io/SPACE-Tag-HD-protocol/`. Pages requires the repository to be public.

## Relationship to SPACE-Tag

The regular-Visium version is at
[chaoyan115/SPACE-Tag-protocol](https://github.com/chaoyan115/SPACE-Tag-protocol). Day 1 is shared
between the two. Day 2 differs: on regular Visium the tissue sits directly on the barcoded slide, so
reverse transcription happens in the same wells used for tagmentation and IVT. On Visium-HD the
tissue slide and the barcoded slide are separate, and the IVT product is moved between them on the
CytAssist. The H&E workflow also differs, and 10x warns against substituting one for the other.

## Feedback

Corrections, questions, and reports of what did or did not work in your hands are welcome. Open an
[issue](https://github.com/chaoyan115/SPACE-Tag-HD-protocol/issues) or start a
[discussion](https://github.com/chaoyan115/SPACE-Tag-HD-protocol/discussions).

## Editing workflow

Edit `protocol.md` only. Everything else is generated or is styling.

```bash
cd /gpfs/commons/home/cyan/data/7_space_tag_hd/5_wiki/SPACE-Tag-HD-protocol

make html   # pandoc protocol.md -> index.html (the published web page)
make docx   # pandoc protocol.md -> SPACE-Tag-HD-protocol.docx
make push   # git add -A, commit with today's date, git push
make all    # build html + docx, then push
```

`make all` is the usual command. It rebuilds both outputs before pushing, so the committed files
always match the current `protocol.md`.

## First-time setup

```bash
pandoc --version
# if missing:
/gpfs/commons/home/cyan/.local/bin/micromamba install -n base -c conda-forge pandoc -y
```

## Optional: custom Word styles

Place a `reference.docx` in this folder and `make docx` picks it up automatically as a formatting
template.

## Source documents

Day 2 follows two 10x Genomics documents, cited by page throughout the protocol:

- *Visium HD 3' Fresh Frozen Tissue Preparation Handbook*, CG000804 Rev A (fixation, H&E, imaging)
- *Visium HD 3' Spatial Gene Expression User Guide*, CG000805 Rev B (slide wash, destaining, CytAssist, RT)
