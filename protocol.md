# SPACE-Tag-HD Protocol: Spatial Chromatin Profiling

SPACE-Tag integrates spatial barcoding  with CUT&Tag-based epigenomic profiling. Antibody-guided PA-Tn5 tagmentation generates transcribable DNA fragments at target chromatin loci, which are then spatially captured via in vitro transcription and reverse transcription on the Visium-HD slide.

**Tags:** Spatial Epigenomics | CUT&Tag | Visium | PA-Tn5 | Histone Modifications  
**Last updated:** September 2, 2026

---

## Solutions & Reagents

Prepare all buffers fresh or as needed. Store at 4°C unless otherwise noted.

### digi-CT Wash Buffer

| Reagent | Volume | Final Conc. |
|---|---|---|
| 1M HEPES | 200 µl | 20 mM |
| 5M NaCl | 300 µl | 150 mM |
| 6.4M spermidine | 0.78 µl | 0.5 mM |
| Protease inhibitor | 1 tablet | 1x |
| 5% digitonin | 20 µl | 0.01% |
| H₂O | to 10 ml | — |

### digi-300-Wash Buffer

> Higher NaCl (300 mM) reduces non-specific Tn5 binding during tagmentation.

| Reagent | Volume | Final Conc. |
|---|---|---|
| 1M HEPES | 200 µl | 20 mM |
| 5M NaCl | 600 µl | 300 mM |
| 6.4M spermidine | 0.78 µl | 0.5 mM |
| Protease inhibitor | 1 tablet | 1x |
| 5% digitonin | 20 µl | 0.01% |
| H₂O | to 10 ml | — |

### Tagmentation Buffer

| Reagent | Volume |
|---|---|
| digi-300-wash buffer | 1000 µl |
| 1M MgCl₂ | 10 µl (10 mM final) |

> MgCl₂ is required for Tn5 transposase activity.

### 2x Primer Hybridization Buffer

| Reagent | Volume | Final Conc. |
|---|---|---|
| 20X SSC | 2 ml | 4X SSC |
| 100% Formamide | 4 ml | 40% |
| 10% Tween-20 | 200 µl | 0.2% |
| H₂O | to 10 ml | — |

### Additional Reagents Required

- 1X PBS
- 1X PBS with 1.25 M Glycine
- BD Perm/Wash Buffer (554723)
- 40 mM EDTA
- ArrayIT 16-well Hybridization Cassettes (AHC1X16) or Proplate (244864, Grace Biolabs)

### Visium-HD Specific Items (10x Genomics)

Catalog numbers from the *Visium HD 3' Spatial Gene Expression User Guide* (CG000805 Rev B, pp. 9–11)
and the *Visium HD 3' Fresh Frozen Tissue Preparation Handbook* (CG000804 Rev A, pp. 5–6). "PN" is
the component part number, which is what is printed on the tube; the kit PN is what is ordered.

**Top-level kit: Visium HD 3', 6.5 mm, 4 rxns — PN-1000857** (also sold as a 16 rxn kit). It contains
the four kits below.

**Visium HD Slide, 6.5 mm, 2 rxns — kit PN-1000670** (store at −80°C)

| Component | PN | Used in |
|---|---|---|
| Visium HD Slide, 6.5 mm | 2000970 | Steps 11, 13, 14, 15 |

**Visium Slide Cassettes S3, 6.5 mm, 2 pk — kit PN-1000847** (ambient)

| Component | PN | Used in |
|---|---|---|
| Visium 2-port, 6.5 mm, Top, 2 pk | 2001252 or 3002329 | Steps 11, 13 |
| Visium Cassette Bottom, 2 pk | 2001344 or 3002328 | Steps 11, 13 |
| Visium Slide Seals, 12 pack | 2000283 | Steps 11, 14, 15 |

**Visium HD 3' Reagents Kit A, Small — kit PN-1000854** (store at −20°C)

| Component | PN | Used in |
|---|---|---|
| Enhancer | 2000482 | Step 9 (Enhancer Mix) |
| Reducing Agent B | 2000087 | Steps 9, 13, 14 |
| RNase Inhibitor B | 2001400 | Step 9 (washes, Mounting Medium) |
| Pre-equilibration Buffer | 2001399 | Step 11 |
| Perm Enzyme B | 3000553 | Step 13 |
| Perm Buffer | 2001398 | Steps 12, 13 |

**Visium HD 3' Reagents Kit B, Small — kit PN-1000855** (store at −20°C)

| Component | PN | Used in |
|---|---|---|
| RT Reagent | 2000086 | Step 14 |
| RT Enzyme G | 2001438 | Step 14 |
| Template Switch Oligo B | 2001027 | Step 14 |

> Kit B also ships Second Strand Enzyme (2000183), Second Strand Reagent (2000219), Second Strand
> Primer (2000217), cDNA Primers (2000089), Amp Mix (2000103), Fragmentation Enzyme (2000104),
> Fragmentation Buffer (2000091), DNA Ligase (220131), and Ligation Mix (2001109). **SPACE-Tag does
> not use any of these.** From Step 16 onward the protocol uses its own second strand synthesis, and
> library construction is by PCR1 plus index PCR rather than 10x fragmentation and ligation.

**Accessories**

| Item | PN | Kit PN |
|---|---|---|
| Visium CytAssist Alignment Aid, 6.5 mm | 3002814 | 1000886 |
| Low Profile Thermocycler Adapter | 3000823 | 1000499 |
| 10x Magnetic Separator | 2001212 | 1000499 |

**Instrument.** Visium CytAssist running **firmware 2.0.0 or higher**.

**Non-10x items.** 20X SSC, 8 M KOH, 0.1 N HCl, 1X or 10X PBS, Low TE Buffer, Qiagen Buffer EB,
methanol, acetone, glycerol, Gill II Hematoxylin, Bluing Buffer, **alcoholic Eosin used undiluted**,
seven 1 L beakers, slide mailers, forceps, a 25 ml reagent reservoir, wide-bore pipette tips,
coverslips, blank slides, lint-free laboratory wipes, and 37°C and 65°C temperature-controlled
instruments. The regular-Visium eosin dilution in Tris-acetic acid buffer is not used in the HD
workflow. **10x does not publish catalog numbers for these in either document**; tested third-party
part numbers, pipette tips, thermal cyclers, and blank slides are listed only in the Visium HD 3'
Protocol Planner (CG000803), and 10x notes that substituting untested items may affect performance.

## Day 0 — Preparation

### A. Adapter Annealing (can be done in advance)

#### Adapter Sequences

HPLC purification recommended; alternatively order in ultramer format.

| Name | Sequence (5'→3') |
|---|---|
| dual_ME19_polyT_v2 (Adapter A) | `TTTTTTTTTTTTTTTTTTTTTTTTTTTTTTVNAGATGTGTATAAGAGACAG` |
| T7_MedsB (Adapter B) | `GAATTTAATACGACTCACTATAGGGAGAGTCTCGTGGGCTCGGAGATGTGTATAAGAGACAG` |
| ME_19_Phos (Mosaic Ends) | `/5Phos/CTGTCTCTTATACACATCT` |

#### Annealing Recipe (per adapter)

| Reagent | Volume |
|---|---|
| Adapter A or B (100 µM stock) | 25 µl |
| Mosaic ends | 25 µl |
| 50x annealing buffer (0.5 M Tris pH 8.0, 2.5 M NaCl) | 1 µl |

#### Annealing Program

- 95°C for 5 min
- Ramp down to 14°C at −0.1°C/s (slow cool for proper duplex formation)

> **Storage:** Aliquot annealed adapters into 2 µl single-use stocks and store at −20°C. Use a fresh aliquot for each experiment.

### B. PA-Tn5 Dilution & Transposon Assembly

#### PA-Tn5 Dilution

Dilute PA-Tn5 to **0.5 mg/ml** using dilution buffer:

**Dilution buffer:** 50% glycerol, 10 mM Tris-HCl pH 7.5, 100 mM NaCl, 0.1 mM EDTA, 1 mM DTT

---

## Day 1 — Protocol Steps
### Step 0: Load the PA-Tn5

> **Rationale:** I found freshly loaded Transposome works the best (highest activity and more stable)

**Transposome assembly:**

1. Mix 10 µl of 0.5 mg/ml PA-Tn5 with 2 µl of annealed adapter aliquot (one per adapter).
2. Incubate at RT for 1 hr.

### Step 1: Formaldehyde Tissue Fixation

> **Rationale:** Light formaldehyde fixation preserves tissue morphology and protein–chromatin interactions while maintaining antibody/enzyme accessibility in subsequent steps.

**Before experiment:**

a. Prepare **0.2% formaldehyde** (methanol-free, Sigma F8775-25ML) in PBS.  
b. Set thermomixer to **37°C** and allow to equilibrate for 5 min.

**Tissue fixation:**

1. Section tissue onto the capture area of a Superfrost™ Plus Microscope Slides (22-037-246, Fisher, draw capture areas at the back of slides according to the cassete you are going to use) at a thickness of **10 µm**.
2. Place the slide (tissue surface up) on the thermomixer. Incubate for 5 min at 37°C.
3. Remove the slide; wipe excess liquid from the back without touching tissue sections.
4. Apply **1 ml of 0.2% formaldehyde** in 1xPBS to cover the tissue. Incubate at RT for 10 min.
5. Wash with **1 ml of 1X PBS + 1.25 M glycine** to quench residual formaldehyde, then remove.
6. Quickly wash with **1 ml of 1X PBS** for ~2 min at RT.

---

### Step 2: Permeabilization

1. Prepare **1x BD Perm buffer** on ice.
2. Apply **70 µl** 1x BD Perm buffer to each well.
3. Incubate for **30 min at 4°C** (in referigerater).

---

### Step 3: Primary Antibody Staining

1. After removing BD Perm buffer, apply **70 µl** primary antibody diluted in 1X BD Perm buffer.
2. Incubate at **RT for 1 hr**.
3. Wash with **100 µl 1x PBS** for 5 min at RT.

> **Note:** Dilution factor should be benchmarked by immunostaining and a pilot experiment.

---

### Step 4: Secondary Antibody Staining

> **Rationale:** The secondary antibody bridges the primary antibody to PA-Tn5, enabling targeted tagmentation at chromatin loci of interest.

1. Add secondary antibody in **digi-CT wash buffer** at **1:50 dilution**, 70 µl/well. Incubate at RT for 30 min.
2. Wash with **100 µl digi-CT wash buffer** for 5 min at RT.

---

### Step 5: Tagmentation

> **Rationale:** PA-Tn5 loaded with sequencing adapters inserts adapters at antibody-bound chromatin sites. Higher salt during binding reduces non-specific insertion; MgCl₂ activates Tn5 during tagmentation.

1. Add loaded PA-Tn5 in **70 µl digi-300-wash buffer** (1:50 dilution). Incubate for **1 hr at RT**.
2. Wash with **digi-300-wash buffer** for 5 min at RT.
3. Add **tagmentation buffer** (10 mM MgCl₂ in digi-300-wash buffer).
4. Incubate at **55°C for 1 hr** (no shake).

> **Recommended:** Start ramping down temperature at 55 min from 55°C → 37°C before stopping, optionally additionally 5min for the temperature to ramp down fully.

---

### Step 6: Tissue Clearing

> **Rationale:** HCl treatment removes histones and bound Tn5, improving accessibility for Gap Filling reaction and *in vitro* transcription.

1. Remove the Tagmentation Reaction.
2. Add **70 µl of 0.1 M HCl** (accurately diluted from stock) to each well.
3. Incubate for **2 min at RT**.
4. Remove HCl. 
5. Add **100 µl of 1X NEB buffer 2** and incubate for 5 min at RT.

> **note:** the 2min clearing here is optimized for mouse brain tissue, for other tissue types, this time might needs optimization.

---

### Step 7: Gap Filling

> **Rationale:** Tagmentation creates nicked DNA ends. Gap filling repairs these nicks, enabling downstream in vitro transcription for signal amplification.

**Gap-Fill Solution (70 µl/well):**

| Reagent | Volume |
|---|---|
| H₂O | 56.8 µl |
| 10x NEB buffer 2 | 7 µl |
| dNTPs | 3.5 µl |
| RNase Inhibitor (RNAseout) | 0.7 µl |
| Klenow (exo⁻) | 2 µl |

1. Remove buffer; add 70 µl fill-in solution. Incubate at **37°C for 30 min** without shaking.
5. Add **100 µl of 1X T7 buffer** and incubate for 5 min at RT.

> A Thermotop is recommended for even temperature distribution.

---

### Step 8: *In Vitro* Transcription

> **Rationale:** T7 RNA polymerase transcribes from the inserted T7 promoter, generating multiple RNA copies per tagmentation event — a key amplification step that increases sensitivity.

**IVT Solution (70 µl/well):**

| Reagent | Volume (µl) |
|---|---|
| nuclease-free water | 35.0 |
| 5× Thermo EP0111 buffer (COMMERCIAL) | 14.0 |
| 25 mM-each rNTP (NEB N0466) | 11.2 |
| 200 mM MgCl₂ working stock | 5.6  |
| RNase inhibitor | 3.5  |
| T7 (Thermo EP0111), 1% | 0.7  |

1. Remove T7 buffer and apply **70 µl IVT solution** to each well.
2. Seal wells with film and incubate in thermomixer at **37°C overnight** (14–16 hrs).

> A thermotop is recommended to maintain temperature uniformity.

---

## Day 2

> **Workflow change vs regular Visium.** In SPACE-Tag on regular Visium the tissue sits directly on
> the barcoded slide, so RT is performed in the same wells used for tagmentation and IVT. On
> Visium-HD the tissue slide and the barcoded slide are separate: IVT-generated RNA is transferred
> from the tissue slide onto the Visium HD Slide on the Visium CytAssist instrument, and all
> downstream enzymology happens on the HD slide. Steps 9 and 10 follow the *Visium HD 3' Fresh
> Frozen Tissue Preparation Handbook* (10x Genomics **CG000804 Rev A**) and Steps 11 to 15 follow the
> *Visium HD 3' Spatial Gene Expression User Guide* (10x Genomics **CG000805 Rev B**); page numbers
> are cited per step. The H&E workflow itself changed between regular Visium and Visium-HD, so the
> fixative, the Enhancer step, the eosin format, and the coverslipping requirement all differ from
> the regular-Visium SPACE-Tag protocol.

> **Timing.** The Visium HD Slide wash (Step 11) takes ~60 min and **must not sit in
> Pre-equilibration Mix for more than 60 min** before the CytAssist run. Start the slide-mailer thaw
> (30 min to 3 h at RT) before H&E staining, and run the wash while the tissue slide is being imaged.

---

### Step 9: Fixation & Enhancer Treatment (tissue slide)

> **Rationale:** Methanol/acetone fixation immobilises IVT-generated RNA on the tissue slide before
> staining. The post-fixation and post-Enhancer washes carry Reducing Agent B and RNase Inhibitor B
> to protect the RNA through the aqueous staining steps.
> Source: CG000804 Rev A, 2.3 Reagent Preparation and 2.5 Fixation, pp. 38–46.

> **This replaces the regular-Visium methanol/isopropanol fixation.** 10x changed the H&E workflow
> between regular Visium and Visium-HD: the fixative, the Enhancer step, the eosin format, and the
> requirement to coverslip are all different. Substituting the regular-Visium H&E here is explicitly
> warned against in CG000804 Rev A, p. 53.

1. **Reagent preparation (before starting; buffers fresh; volumes are for up to two tissue slides transferred to one VisiumHD slide):**

Clean the workspace, pipettes, and gloves with RNase decontamination solution followed by 70% ethanol.
Pre-heat one temperature-controlled instrument to **37°C** and one to **65°C**.

a) *Fixation Solution* (invert gently to mix; may be made up to 24 h ahead and stored at −20°C):

| Reagent | Stock | Final | Total (ml) |
|---|---|---|---|
| Methanol | 100% | 50% | 5.0 |
| Acetone | 100% | 50% | 5.0 |
| **Total** | | | **10.0** |

Dispense the 10 ml into a slide mailer labelled **Fixation Solution Mailer** and move it to **−20°C**.
Do not take it out until immediately before use.

b) *Water beakers.* Clean **seven 1 L beakers** (RNase decontamination solution 10 sec to 1 min → 70%
isopropanol or ethanol → Milli-Q rinse) and dispense **800 ml Milli-Q water** into each. Beakers 1 to 6
are used in Step 10; keep beaker 7 for coverslip removal in Step 12.

c) *Alcoholic Eosin.* Dispense **10 ml undiluted alcoholic Eosin** into a slide mailer, one mailer per slide.

d) *1X PBS* (two 50 ml tubes, 100 ml total, at RT):

| Reagent | Stock | Final | Total (ml) |
|---|---|---|---|
| Nuclease-free water | — | — | 45.0 |
| PBS | 10X | 1X | 5.0 |
| **Total** | | | **50.0** |

Fill two 2 ml tubes with 1X PBS and warm at **37°C for 10 min**; hold at 37°C for the Enhancer Mix.

e) *Mounting Medium* (2 ml tube, add in the order listed; use a wide-bore tip for glycerol; vortex, then
centrifuge until no bubbles remain). For Reducing Agent B, make an intermediate dilution rather than
pipetting 0.2 µl (for example 2 µl of a 1:10 dilution):

| Reagent | 10x PN | Stock | Final | 1 Slide (µl) | 2 Slides + 10% (µl) |
|---|---|---|---|---|---|
| Glycerol | — | 100% | 85% | 85.0 | 187.0 |
| Reducing Agent B | 2000087 | — | — | 0.2 | 0.4 |
| RNase Inhibitor B | 2001400 | — | — | 10.0 | 22.0 |
| Nuclease-free water | — | — | — | 4.8 | 10.6 |
| **Total** | | | | **100.0** | **220.0** |

f) *Post Fixation Wash* (15 ml tube, add in the order listed, vortex, hold at RT). **Label as Tube 1:**

| Reagent | 10x PN | 1 Slide (µl) | 2 Slides + 5% (µl) |
|---|---|---|---|
| 1X PBS | — | 1,320 | 2,772 |
| Reducing Agent B | 2000087 | 30 | 63 |
| RNase Inhibitor B | 2001400 | 150 | 315 |
| **Total** | | **1,500** | **3,150** |

g) *Post Enhancer Wash* (15 ml tube, add in the order listed, vortex, hold at RT). **Label as Tube 3**
(Tube 2 is prepared during the protocol):

| Reagent | 10x PN | 1 Slide (µl) | 2 Slides + 5% (µl) |
|---|---|---|---|
| 1X PBS | — | 1,796.0 | 3,771.6 |
| Reducing Agent B | 2000087 | 4.0 | 8.4 |
| RNase Inhibitor B | 2001400 | 200.0 | 420.0 |
| **Total** | | **2,000.0** | **4,200.0** |

h) *Enhancer* (**PN-2000482**, Kit A 1000854). Place on ice, then reconstitute at **65°C for 10 min**, or until the solution
is a dark green with no visible particulates. **DO NOT exceed 20 min.**

- *First thaw:* vortex briefly and aliquot into four 1.5 ml tubes at **430 µl** each. Hold the aliquot
  in use at RT, inverting gently every 10 min; move the rest to ice, then store at −20°C.
- *Frozen aliquot:* 65°C for 10 min as above, then hold at RT, inverting gently every 10 min.
- **DO NOT exceed 2 freeze-thaw cycles per aliquot.**

Obtain a **25 ml reagent reservoir**; the same reservoir is used throughout. Retrieve the Fixation
Solution Mailer from −20°C and keep it on ice.

**Fixation:**

> Pipette at least **1 cm from the tissue edge** and do not pipette at an angle, so the tissue is not disturbed.

1. Remove the IVT solution and disassemble the gasket/cassette from the tissue slide.
2. Gently immerse the slide in the Fixation Solution Mailer on ice. Incubate **1 min**.
3. Remove the slide, flick, and wipe excess fixative from the back with a lint-free wipe. **DO NOT touch the tissue sections.**
4. Place the slide tissue-side up over the reagent reservoir and air dry **1 min**. No more than two slides per reservoir.
5. Add **750 µl Tube 1 (Post Fixation Wash)** to each tissue section, then a further **750 µl**, for **1.5 ml total per section**.
6. Incubate **10 min at RT**.
7. During the incubation, prepare **Tube 2 (Enhancer Mix)** in a 15 ml tube. Vortex. Hold at **37°C**:

| Reagent | 10x PN | 1 Slide (µl) | 2 Slides + 5% (µl) |
|---|---|---|---|
| Pre-warmed 1X PBS | — | 1,800 | 3,780 |
| Enhancer | 2000482 | 200 | 420 |
| **Total** | | **2,000** | **4,200** |

8. Remove the Post Fixation Wash by tilting the slide over the reservoir. Do not let the slide touch liquid already in the reservoir.
9. Place the slide tissue-side up over the reservoir. **DO NOT allow the slide to dry** at any point from here to coverslip mounting.
10. Add **1 ml Tube 2 (Enhancer Mix)** to cover the sections uniformly, then **immediately** remove it by tilting.
11. Add a second **1 ml Tube 2 (Enhancer Mix)**. Incubate **1 min at RT**, then remove by tilting.
12. Add **1 ml Tube 3 (Post Enhancer Wash)** to cover the sections uniformly, then **immediately** remove it by tilting.
13. Add a second **1 ml Tube 3 (Post Enhancer Wash)**. Incubate **1 min at RT**, then remove by tilting.
14. Proceed immediately to Step 10.

> **SPACE-Tag notes (untested).** Two points in this step have not been benchmarked on SPACE-Tag
> material. First, the handbook's **1 min** fixation is set for an unfixed cryosection, where
> methanol/acetone both fixes and permeabilises; here the tissue is already formaldehyde-fixed and
> the only job of this step is to hold free IVT RNA in place, which the previous protocol did with
> 30 min of methanol at −20°C. Second, the Enhancer is a proprietary reagent developed for the HD 3'
> mRNA assay and its effect on IVT RNA retention is unknown. If capture is low, test a lengthened
> fixation and an Enhancer-omitted arm as paired sections on the same slide, read out as unique
> fragments per bin.

---

### Step 10: H&E Staining, Coverslip Mounting & Imaging (tissue slide)

> **Rationale:** H&E staining provides the histology image that Space Ranger aligns to the CytAssist
> image. Coverslipping in the RNase-protected glycerol Mounting Medium is required by the HD
> workflow: the CytAssist run in Step 13 begins from a coverslipped, mounted slide.
> Source: CG000804 Rev A, 2.6 H&E Staining, 2.7 Coverslip Mounting, 2.8 Imaging, pp. 47–50.

> Pipette at least **1 cm from the tissue edge** and do not pipette at an angle.
> **Work quickly.** Slow progress through these steps causes RNA degradation.

**Staining:**

1. Place the slide tissue-side up over the reagent reservoir. No more than two slides per reservoir.
2. Add **1 ml Hematoxylin** (Gill II) per slide to cover all sections uniformly. Incubate **1 min at RT**.
3. Discard by holding the slide at an angle over the reservoir.
4. Immerse **5×** in Water Beaker 1, **15×** in Beaker 2, **15×** in Beaker 3.
5. Wipe excess liquid from the back of the slide with a lint-free wipe, without touching the sections.
6. Place the slide tissue-side up over the reservoir. Add **1 ml Bluing Buffer** per slide. Incubate **1 min at RT**, then discard at an angle.
7. Immerse **10×** in Water Beaker 4. Wipe the back of the slide.
8. Gently immerse the slide in the **undiluted alcoholic Eosin** mailer, one mailer per slide. Incubate **30 sec at RT**.

> **DO NOT use diluted Eosin.** The regular-Visium eosin dilution in Tris-acetic acid buffer does not apply to the HD workflow.

9. Discard by holding the slide at an angle with its bottom edge against a lint-free wipe.
10. Immerse for **30 sec** in Water Beaker 5, then **10×** in Water Beaker 6. Wipe the back of the slide.
11. Proceed immediately to coverslip mounting. **DO NOT air dry the slide.**

**Coverslip Mounting:**

12. Gently touch the long edge of the slide to a lint-free wipe to remove excess moisture, including any large droplets.
13. Place the slide on a flat, clean, non-absorbent surface. Some residual droplets are expected. **DO NOT allow the slide to dry.**
14. Using a **wide-bore tip**, add **100 µl Mounting Medium** to cover the entire tissue section.

> **DO NOT use Cytoseal or nail polish** to secure the coverslip. The Mounting Medium must remain removable in water at Step 12.

15. Apply the coverslip slowly, at an angle from one end, without introducing bubbles. Let the Mounting Medium spread and settle.
16. Wick away any large excess of Mounting Medium from the coverslip edge with a lint-free wipe. Do not move the coverslip.
17. Proceed immediately to imaging, or lay the slide flat in a slide holder in the dark at **4°C for up to 24 h**. Laying flat prevents loss of Mounting Medium.

**Imaging:**

18. If the slide was stored, remove condensation from the back with a lint-free wipe.
19. Image the tissue section at the desired magnification using brightfield settings (Metafer scope; see also CG000688 for HD imaging requirements).
20. If using the Visium CytAssist Alignment Aid to annotate the slide, do so **while the slide is still coverslipped**, before Step 12.
21. Lay the slide flat in a slide holder in the dark at **4°C** and proceed to Step 11. Slides must stay at 4°C until coverslip removal in Step 12, for **up to 72 h**. **DO NOT let the coverslip dry out.**

---

### Step 11: Visium HD Slide Wash & CytAssist Preparation

> **Rationale:** The Visium HD Slide is thawed, washed free of storage buffer, and equilibrated in
> Pre-equilibration Buffer immediately before the CytAssist run.
> Source: CG000805 Rev B, 1.1 Visium HD Slide Wash, pp. 49–54.

> **DO NOT** touch the Visium HD Slide spacer during the washes.

**a. Thaw.** Remove the Visium HD Slide mailer from −80°C and from its mylar bag. **DO NOT uncap.**
Keep upright and thaw at RT for **30 min to 3 h**. Prepare one Visium HD Slide at a time.

**b. 0.1X SSC Buffer** (two 50 ml centrifuge tubes, 80 ml total; sufficient for the whole protocol):

| Reagent | Stock | Final | 1 Visium HD Slide + 15% |
|---|---|---|---|
| Nuclease-free water | — | — | 39.8 ml |
| SSC | 20X | 0.1X | 0.2 ml |
| **Total** | | | **40.0 ml** |

**c. Pre-equilibration Mix** (pipette mix, centrifuge briefly, keep at RT):

| Reagent | 10x PN | 1 Visium HD Slide + 10% |
|---|---|---|
| Nuclease-free water | — | 55 µl |
| Pre-equilibration Buffer | 2001399 | 55 µl |
| **Total** | | **110 µl** |

**Wash:**

1. Open the slide mailer. Add **7 ml 0.1X SSC** slowly along the side of the mailer on one side of the slide, then **7 ml** on the other side, so both faces are immersed.
2. Incubate at RT for **1 min**. **DO NOT close the mailer.** Pour off the SSC while holding the slide in place with one finger.
3. **Three 5-min washes:** repeat the 7 ml + 7 ml addition, incubate **5 min at RT**, and pour off. Do this three times. During the third wash, keep the SSC in the mailer in case the slide needs re-immersion.
4. Remove the slide and inspect for debris. If debris is visible, briefly re-immerse in the mailer and remove.
5. Flick the slide. Dry the back (the side without spacers) with a lint-free wipe if needed.
6. Gently touch the long edge of the slide to a fresh lint-free wipe **5×** to remove excess SSC. Re-inspect; repeat immersion, flicking, and wiping if particulate remains.
7. **Record the Visium HD Slide serial number.**
8. Place the slide in a new **6.5 mm Visium Cassette** (Visium Slide Cassettes S3 kit **1000847**: top **2001252** or **3002329**, bottom **2001344** or **3002328**; assembly per CG000730).
9. Add **100 µl 0.1X SSC** to each well, then remove it. **Repeat the removal** to ensure no SSC remains.
10. Add **50 µl Pre-equilibration Mix** to each well.

> **DO NOT exceed 60 min** between adding Pre-equilibration Mix and starting the CytAssist run.

11. Apply a new **Visium Slide Seal** (**PN-2000283**) to the cassette.
12. Power on the Visium CytAssist (**firmware 2.0.0 or higher required**). Press **New Run** and enter the slide serial number, run name, and **37°C for 30 min**.
13. Enter sample names and positions (**A1 = right side, D1 = left side**).

---

### Step 12: Destaining (tissue slide)

> **Rationale:** Acid destaining removes hematoxylin so that residual stain does not transfer to the
> Visium HD Slide during the CytAssist run.
> Source: CG000805 Rev B, 2.2 Destaining, pp. 59–60.

**Before starting:** dispense **10 ml 0.1 N HCl** into a labelled HCl slide mailer and **10 ml 1X PBS**
into a PBS mailer, both freshly prepared in nuclease-free water. Each volume is sufficient for two
tissue slides. **DO NOT reuse either solution.** A 50 ml centrifuge tube may be substituted, holding
no more than two slides placed back to back with tissue facing outward, provided the tissue is fully
submerged.

**Coverslip removal (CG000805 Rev B, 2.1, p. 58).** Perform this before destaining.

1. Immerse the slide sideways in a clean 1 L beaker holding **800 ml Milli-Q water** (Water Beaker 7 from Step 9), with the coverslipped face fully sideways so the coverslip cannot drag across the tissue.
2. Hold the slide in the water until the coverslip separates on its own.

> To avoid tissue damage or detachment, **DO NOT** move the slide up and down, shake it, or move the coverslip by hand.

3. Gently immerse the slide **30×** in the water to remove all Mounting Medium.
4. Proceed immediately to destaining. **DO NOT allow the slide to dry.**

**Destaining:**

1. Immerse the slide **10×** in the 0.1 N HCl mailer.
2. Immerse the slide in the HCl mailer, close the mailer, and incubate for **15 min at RT**.
3. **During the HCl incubation, prepare the Permeabilization Mix** (Step 13b). Pipette mix until homogeneous, avoid bubbles, keep at RT.
4. Immerse the slide **10×** in the 1X PBS mailer.
5. Immerse the slide in the PBS mailer and incubate for **5 min at RT**.
6. Remove the slide and immediately flick to remove excess PBS. Inspect for large droplets and repeat flicking if present.
7. Once no droplets remain on the tissue surface, remove excess PBS outside the tissue with a lint-free wipe, without touching the sections.
8. Gently tap the back of the slide onto a fresh lint-free wipe.
9. Place the slide tissue-side up on a lint-free wipe on a flat, clean surface and **proceed immediately to Step 13**.

---

### Step 13: CytAssist-Enabled RNA Transfer

> **Rationale:** The tissue slide and the Visium HD Slide are brought into contact on the CytAssist.
> IVT RNA released from the tissue is captured by the poly(dT) oligos on the 2 µm barcoded squares of
> the HD Capture Area.
> Source: CG000805 Rev B, 3.1 CytAssist-Enabled Poly(A) RNA Capture, pp. 64–72.

**a. Visium HD Slide steps**

1. Retrieve the Visium Cassette. Remove the Visium Slide Seal and remove the Pre-equilibration Mix: hold the cassette at **45°**, tilted right so buffer pools in the lower right corner of the well; with a P200 set to 200 µl, place the tip in the bottom right corner without scratching the fiducial frame or hydrogel, and aspirate. Repeat with a fresh tip, then do the same for the other well.

> Failure to remove the Pre-equilibration Mix completely delays slide drying and reduces assay performance.

2. Remove the top half of the cassette, leaving the slide in the bottom half. Rest the top half gasket-side up to keep it free of debris.
3. Remove the Visium HD Slide from the cassette without touching the active surface. Dry the back with a lint-free wipe if needed. **DO NOT flick the slide.** Save the cassette for reuse after the run.
4. Load the slide against the grooves of the Visium Slide Stage and close the Visium Slide Lock.
5. Allow the slide to **dry on the stage for 10 min**. Inspect the entire spacer chamber from several angles; if any liquid remains, continue drying and proceed the moment the chamber is dry.

**b. Permeabilization Mix** (prepared during the HCl incubation in Step 12):

| Reagent | 10x PN | 2 Tissue Slides (µl, incl. overage) |
|---|---|---|
| Nuclease-free water | — | 10.4 |
| Perm Buffer | 2001398 | 20.0 |
| *(added immediately before the run:)* | | |
| Reducing Agent B | 2000087 | 1.6 |
| Perm Enzyme B | 3000553 | 8.0 |
| **Total** | | **40.0** |

**c. Tissue slide loading**

6. Gently tap the back of the tissue slide onto a lint-free wipe. If Alignment Aid marks were drawn, tap rather than wipe so the marks are not removed.
7. Load the tissue slide into the CytAssist, keeping the frosted area outside the dashed zone on the tissue slide stage. **Both the tissue slide and the Visium HD Slide must be completely dry** before the run; examine from multiple angles.

**d. Reagent addition and run**

8. Pipette mix Perm Enzyme B (**PN-3000553**) and vortex Reducing Agent B (**PN-2000087**); centrifuge both briefly. Add **1.6 µl Reducing Agent B** and **8 µl Perm Enzyme B** to the 30.4 µl Permeabilization Mix. Pipette mix 15× with the pipette set to 30 µl, avoiding bubbles. Centrifuge 5 sec.

> Start the run **within 5 min** of adding Perm Enzyme B and Reducing Agent B.

9. Slowly aspirate **17 µl** of completed Permeabilization Mix and check the tip for bubbles. Slowly dispense **17 µl** into the centre of each spacer well on the Visium HD Slide, using a fresh tip per dispense. Do not push the plunger past the first stop.
10. Close the lid, press **Next**, then press **play**. Run at **37°C for 30 min**.
11. At the end of the run, press **Done** and open the lid. **DO NOT** leave the sample in the instrument. **DO NOT** power off the instrument yet. It is normal for stain or tissue to remain on the tissue slide.
12. Immediately remove the Visium HD Slide.

**e. Five 0.1X SSC rinses** (perform next to the instrument so the Capture Areas are washed promptly)

13. Holding the slide over a liquid waste container, rinse each Capture Area with **1 ml 0.1X SSC**. **DO NOT pipette directly onto the Capture Areas.** Repeat for a total of **five rinses**. If pink stain remains, continue rinsing until it is gone.
14. Gently touch the long edge of the slide to a lint-free wipe **3–5×** to remove excess SSC. **DO NOT touch the Capture Area.**
15. Place the Visium HD Slide back into the same Visium Cassette. Some residual moisture is normal.
16. Proceed immediately to Step 14.

---

### Step 14: Reverse Transcription (Visium HD Slide)

> **Rationale:** Two sequential RT reactions convert the captured IVT RNA into spatially barcoded
> cDNA on the HD slide. RT1 at 53°C favours read-through on structured template; RT2 at 42°C with a
> higher enzyme load extends conversion.
> Source: CG000805 Rev B, 3.2 Reverse Transcription, pp. 69–74.
> RT Enzyme G is the Visium-HD enzyme and is **not** interchangeable with RT Enzyme D (2000216/2000227)
> used in the regular-Visium CytAssist workflow.

**Reagent handling.** Thaw RT Reagent (**PN-2000086**) at RT, vortex, then move to ice. Keep RT
Enzyme G (**PN-2001438**) on ice. Resuspend Template Switch Oligo B (**PN-2001027**) in
**65 µl Low TE Buffer**, vortex 15 sec at maximum speed, and
centrifuge briefly; store resuspended stock at −80°C and thaw on ice for ≥30 min on subsequent uses.

**a. Program the thermal cycler** with a Low Profile Thermocycler Adapter (PN-3000823) in place and start it so it
holds at temperature:

| | Lid | Reaction volume | Run time |
|---|---|---|---|
| **Reverse Transcription 1** | 53°C | 100 µl | 48 min |

| Step | Temperature | Time |
|---|---|---|
| Pre-equilibrate | 53°C | Hold |
| Reverse Transcription 1 | 53°C | 00:45:00 |
| Cool | 4°C | 00:03:00 |
| Hold | 4°C | Hold |

**b. RT Master Mix ** (prepare on ice, add reagents in the order listed, pipette mix 10×, centrifuge briefly, keep on ice):

| Reagent | 10x PN | 1X (µl) | 1 Visium HD Slide (µl, two reactions + overage) |
|---|---|---|---|
| Nuclease-free water | — | 40.2 | 88.4 |
| RT Reagent | 2000086 | 17.5 | 38.5 |
| Reducing Agent B | 2000087 | 1.4 | 3.1 |
| RT Enzyme G | 2001438 | 10.9 | 24.0 |
| **Total** | | **70.0** | **154.0** |

1. Remove any residual 0.1X SSC from the wells.
2. Add **70 µl RT Master Mix ** to each well.
3. Apply a new Visium Slide Seal, place the cassette on the Low Profile Thermocycler Adapter on the pre-heated cycler, and close the lid.
4. Skip the Pre-equilibrate step to start **Reverse Transcription**.

---

### Step 15: Denaturation (post-RT)

> **Rationale:** KOH denaturation removes the RNA template, leaving single-stranded cDNA for second
> strand synthesis.
> Source: CG000805 Rev B, 3.3 Denaturation, p. 74.

**0.08 M KOH** (prepare shortly before use, add reagents in the order listed, vortex, centrifuge
briefly, keep at RT, discard after use):

| Reagent | Stock | Final | 2X + overage (µl) |
|---|---|---|---|
| Nuclease-free water | — | — | 495.0 |
| KOH | 8 M | 0.08 M | 5.0 |
| **Total** | | | **500.0** |

1. At the end of Reverse Transcription 2, remove the cassette from the Low Profile Thermocycler Adapter onto a flat, clean surface.
2. Remove the Visium Slide Seal and pipette out all RT2 mix.
3. Add **75 µl 0.08 M KOH** to each well.
4. Incubate for **5 min at RT**.
5. Remove the KOH.
6. Add **100 µl Buffer EB** (10 mM Tris-Cl, pH 8.5) to each well.

---

### Step 16: Second Strand Synthesis

> **Rationale:** A primer is annealed to the single-stranded cDNA; Klenow polymerase extends it to generate dsDNA suitable for PCR amplification.

**Primer Annealing:**

| Reagent | Volume |
|---|---|
| 2x primer hybridization buffer | 35 µl |
| Primer (1 µM) | 1.4 µl |
| H₂O | 33.6 µl |

1. Add 70 µl of primer annealing mix to each well; incubate at **RT for 30 min**.
2. Wash with Buffer EB: pipette 100 µl into each well and immediately remove.

**Klenow Extension:**

| Reagent | Volume |
|---|---|
| 5x Maxima Buffer | 14 µl |
| Water (RNase/DNase-free) | 40.25 µl |
| dNTP mix (10 mM each) | 7 µl |
| DNA primer (10 µM) | 7 µl |
| Klenow (200 U/µl) | 1.75 µl |
| **Total** | **70 µl** |

1. Add 70 µl of Klenow mix to each well; avoid bubbles. Cover and incubate for **1 hr at 37°C**.
2. Remove the Klenow mix.

---

### Step 17: Denaturation (post-Second Strand)

> **Rationale:** A second KOH denaturation releases the dsDNA from the slide for collection and downstream library preparation.

1. Remove reagents from the wells.
2. Add **100 µl Buffer EB** to each well; remove immediately.
3. Add **35 µl of 0.08 M KOH** (freshly diluted) to each well.
4. Incubate for **10 min at RT**.
5. Add **5 µl of 1 M Tris (pH 7.0)** to each tube in an 8-tube strip to pre-neutralize.
6. Transfer 35 µl of sample from each well to the corresponding Tris-containing tube (±1–2 µl variation expected).
7. Vortex briefly, centrifuge, and place on ice.

---

### Step 18: PCR Library Amplification

> **Rationale:** PCR1 amplifies the cDNA library using primers targeting the capture oligo and Nextera adapter sequences. Index PCR adds sample-specific barcodes for multiplexed sequencing.

**PCR1:**

For Visium slides (e.g. mouse brain, ~70% capture area): ~18 cycles recommended.

| Reagent | Volume |
|---|---|
| Elution | 40 µl |
| cDNA-oligo1 (`CTACACGACGCTCTTCCGATCT`) | 5 µl |
| PF-nexteraR2-DME (`GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAG`) | 5 µl |
| NEBNext | 50 µl |

**PCR1 Program:**

| Step | Temp | Time | Cycles |
|---|---|---|---|
| Initial denaturation | 98°C | 3 min | 1 |
| Denaturation | 98°C | 15 s | 18× |
| Annealing | 60°C | 20 s | 18× |
| Extension | 72°C | 1 min | 18× |
| Final extension | 72°C | 1 min | 1 |
| Hold | 4°C | ∞ | — |

Purify with **1x SPRI**; elute in 50 µl. Use 10 µl for index PCR.

**Index PCR (5 cycles):**

| Reagent | Volume |
|---|---|
| Elution | 10 µl |
| SIPCR-T5XXX | 5 µl |
| N7 indexing primer | 5 µl |
| H2O | 30 µl |
| NEBNext |50 µl |

**Primer sequences:**

- SIPCR-T5XXX: `AATGATACGGCGACCACCGAGATCTACACNNNNNNNNACACTCTTTCCCTACACGACGCTC`
- N7 indexing primer: `CAAGCAGAAGACGGCATACGAGATNNNNNNNNGTCTCGTGGGCTCGG`

**Final Cleanup:**
Run a gel to check product size first, we do see variations on products vs primer dimer distributions.
Perform **1x SPRI purification** twice(target product ~400bp), for pure product
