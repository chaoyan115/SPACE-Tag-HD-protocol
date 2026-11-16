# SPACE-Tag-HD Protocol

Spatial CUT&Tag chromatin profiling adapted to the 10x Genomics Visium-HD platform.

Antibody-guided protein A-Tn5 tagmentation generates transcribable DNA fragments at target chromatin
loci. These are amplified by in vitro transcription and transferred to a Visium HD Slide on the
Visium CytAssist instrument, where they are captured on 2 µm barcoded squares.

**Read the protocol:** [chaoyan115.github.io/SPACE-Tag-HD-protocol](https://chaoyan115.github.io/SPACE-Tag-HD-protocol/).
The source is [protocol.md](protocol.md), and a print-ready Word version is
[SPACE-Tag-HD-protocol.docx](SPACE-Tag-HD-protocol.docx).

## Before your first run

Start with the [protocols home page](https://chaoyan115.github.io/SPACE-Tag-protocol/start.html). It links
all three protocols and shows the order in which to use them:

```
1. Section and check the tissue           H&E on one section
2. Validate the antibody                  immunofluorescence on a plain slide
3. CUT&Tag test on a plain slide          standard Nextera adapters, PCR, gel
4. IVT test on a plain slide              full Day 1, then RNA purification and TapeStation
5. Spatial experiment                     SPACE-Tag (Visium) or SPACE-Tag-HD (Visium HD)
6. Library QC                             fragment analyzer, then a shallow sequencing run
7. Deep sequencing and analysis
```

Steps 2 to 4 use plain glass slides, a gel and one TapeStation run, and catch most failures before a
spatial slide is used. Step 3 is the
[CUT&Tag test](https://chaoyan115.github.io/SPACE-Tag-protocol/cuttag-test.html) and step 4 the
[IVT test](https://chaoyan115.github.io/SPACE-Tag-protocol/ivt-test.html).

## Relationship to SPACE-Tag

The regular-Visium version is at
[chaoyan115/SPACE-Tag-protocol](https://github.com/chaoyan115/SPACE-Tag-protocol). Day 1 is shared
between the two. Day 2 differs: on regular Visium the tissue sits directly on the barcoded slide, so
reverse transcription happens in the same wells used for tagmentation and IVT. On Visium-HD the
tissue slide and the barcoded slide are separate, and the IVT product is moved between them on the
CytAssist. The H&E workflow also differs, and 10x warns against substituting one for the other.

## Citation

If you use SPACE-Tag, please cite:

> Yan C., He R., Fernandez S., Pleska M., Maniatis S., Raimondi I., Vickovic S. SPACE-Tag enables
> high-throughput spatial chromatin profiling with CUT&Tag. *bioRxiv* (2026).
> [doi:10.64898/2026.11.06.764689](https://doi.org/10.64898/2026.11.06.764689)

The preprint is under peer review, and this protocol may be updated as the paper is revised.

## Feedback

Corrections, questions, and reports of what did or did not work in your hands are welcome. Open an
[issue](https://github.com/chaoyan115/SPACE-Tag-HD-protocol/issues) or start a
[discussion](https://github.com/chaoyan115/SPACE-Tag-HD-protocol/discussions).

## Source documents

Day 2 follows two 10x Genomics documents, cited by page throughout the protocol:

- *Visium HD 3' Fresh Frozen Tissue Preparation Handbook*, CG000804 Rev A (fixation, H&E, imaging)
- *Visium HD 3' Spatial Gene Expression User Guide*, CG000805 Rev B (slide wash, destaining, CytAssist, RT)
