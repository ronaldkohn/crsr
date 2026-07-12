# BAM / MDMA research collection

Personal medical-research dossier assembled for a downstream **meta-analysis pass in Fable**.
The owner (ronaldkohn@gmail.com) has **bile acid malabsorption (BAM / bile acid diarrhea, BAD)**,
diagnosed privately after years of NHS delays, and treated successfully (~80% improvement) with
**colesevelam + ondansetron**. He also observes a striking, reproducible *physiological* effect of
**MDMA** on his gut (bloating resolves, bowel-urgency-then-relief, posture straightens, abdominal
muscle tone becomes "like stone"), and hypothesizes a real anti-inflammatory / gut-signalling
mechanism rather than a purely mood effect.

See [`original-prompt.md`](./original-prompt.md) for the verbatim statement of intent and full
clinical history — that is the source of truth for scope.

> ⚠️ **This is a personal research collection, not medical advice and not a clinical record.**
> The PDFs are third-party copyrighted papers kept here for private reference/meta-analysis only.
> MDMA is discussed as a pharmacology/physiology research question; nothing here is a
> recommendation to use it.

---

## What's in here

```
bam/
├── CLAUDE.md                       ← you are here (guide + source manifest)
├── original-prompt.md              ← verbatim session-starting prompt + clinical history
├── bam-mdma-research-dossier.md    ← THE deliverable: 7-section, heavily-cited dossier
└── docs/
    ├── sources/                    ← the 26 primary/authoritative source PDFs
    └── extractions/                ← pdftotext full-text extractions (grep-able, for Fable)
```

- **`bam-mdma-research-dossier.md`** — the main artifact. 7 sections (below), every claim tagged
  with a confidence tier. Built for a machine/meta-analysis pass: data-dense, minimal prose,
  citations inline.
- **`docs/sources/`** — every real source PDF the owner supplied, renamed `Author-Year-topic-Journal`.
- **`docs/extractions/`** — `pdftotext -layout` plain-text extractions of the papers, named to match
  their PDF. These are the grep-friendly copies used to verify every quoted number. Not every source
  has one (some were read via the PDF reader directly); the PDF is always the source of truth.

Misfire uploads (wrong papers the fetcher returned during retrieval — diabetes/ophthalmology/
telerehab/etc.) were **excluded** at the owner's request; they contained nothing on-topic.

---

## The 7 research angles (dossier sections)

1. **BAM pathophysiology & diagnosis** — types 1–4, SeHCAT / serum C4 / FGF19, TGR5 mechanism
2. **Long-term sequestrant treatment trajectories** — colesevelam/cholestyramine, dose-response, RCTs, newer drugs (liraglutide, FXR agonists, aldafermin)
3. **Ondansetron as adjunct** — 5-HT3 antagonism in IBS-D, the Garsed/Gunn Nottingham trials, super-responders on low dose
4. **MDMA pharmacology** — serotonin release, 5-HT3, oxytocin, anti-inflammatory (TNF-α/IL-1β↓, IL-10/TGF-β↑), gut & muscle-tone effects, MAPS/MAPP trial safety data
5. **MDMA ↔ ondansetron / 5-HT3 & serotonin-syndrome interactions**
6. **Bile acid ↔ serotonin / TGR5 / FXR crosstalk** — the dual-arm TGR5 story (pro-motility EC-cell vs anti-motility myenteric), human biopsy data
7. **Adjacent research & gaps** — MAPP GI/muscle AE data, documented open questions

---

## Confidence tiers (used throughout the dossier)

- **USER-PROVIDED PDF — VERIFIED** — full text read directly from a PDF in `docs/sources/`. Highest confidence. **26 papers** are at this tier.
- **CORROBORATED** — triangulated across ≥2 independent searches/snippets but no full text.
- **SNIPPET-ONLY** — single search snippet; treat as a lead, not a fact.
- **CORRECTED / REFUTED** — flagged where an earlier claim was wrong (kept visible on purpose).

**Two honest content gaps** are documented in the dossier and remain open (they are the most
interesting targets for the meta-analysis):
1. No source directly connects **ondansetron / 5-HT3 blockade** to the **bile-acid → TGR5 → EC-cell → 5-HT** loop specifically.
2. No case reports or forum accounts of **BAM/IBS/IBD patients reporting GI improvement on MDMA** — the owner's observation appears undocumented in the literature.

---

## Source manifest (26 verified primary sources)

Grouped by the angle they most support. Filenames below are in `docs/sources/` (`.pdf`) and, where
present, `docs/extractions/` (`.txt`).

### BAM pathophysiology, diagnosis & reviews
| File stem | Citation |
|---|---|
| `Yang-2024-BAD-review-precision-medicine` | Yang et al. 2024 — Bile Acid Diarrhea: molecular mechanisms to clinical dx/tx (review) |
| `DiCiaula-2024-BAM-systematic-review-EJIM` | Di Ciaula et al. 2024, *Eur J Intern Med* — systematic review (defines Type IV) |
| `Slattery-2015-BAM-prevalence-IBS-D-metaanalysis-APT` | Slattery et al. 2015, *Aliment Pharmacol Ther* — BAM prevalence in IBS-D meta-analysis (28.1%) |
| `Sadowski-2020-CAG-guideline-BAD-JCAG` | Sadowski et al. 2020 — Canadian Assoc. Gastroenterology clinical practice guideline (GRADE) |

### Long-term treatment & newer drug classes
| File stem | Citation |
|---|---|
| `Chen-2025-FAERS-sequestrant-pharmacovigilance-PLOSONE` | Chen et al. 2025, *PLOS ONE* — 20-yr FAERS pharmacovigilance of the 3 sequestrants (n=5,286) |
| `Vijayvargiya-2020-colesevelam-gene-expression-RCT-CGH` | Vijayvargiya et al. 2020, *CGH* 18:2962 — colesevelam RCT, colonic FXR/TGR5 gene expression |
| `BouSaba-2022-BAD-IBS-D-QoL-CGH` | BouSaba et al. 2022, *CGH* 20:2083 — BAD-vs-IBS-D symptoms, QoL & depression |
| `BouSaba-2023-aldafermin-FGF19-RCT-Gastroenterology` | BouSaba et al. 2023, *Gastroenterology* 165:499 — aldafermin (FGF19 analogue) RCT |
| `Merza-2024-BAM-treatment-network-metaanalysis-IBD-JCMR` | Merza et al. 2024, *J Clin Med Res* 16:33 — network meta-analysis (7 RCTs); tropifexor #1 for biomarkers, liraglutide #1 for fecal BA. IBD population |
| `Ellegaard-Karhus-2024-liraglutide-colesevelam-bile-acid-levels-CTG` | Ellegaard/Kårhus et al. 2024, *Clin Transl Gastroenterol* — liraglutide vs colesevelam, distinct serum/fecal BA effects (companion to Kårhus 2022 RCT) |
| `Karhus-2023-BAD-epidemiology-Denmark-ClinEpidemiol` | Kårhus et al. 2023, *Clin Epidemiol* 15:1173 — national registry, 5,264 BAD patients; prevalence, comorbidity & socioeconomic burden |

### Ondansetron / 5-HT3 in IBS-D
| File stem | Citation |
|---|---|
| `Garsed-2014-ondansetron-IBS-D-RCT-Gut` | Garsed et al. 2014, *Gut* — ondansetron in IBS-D, randomised crossover RCT (Nottingham) |
| `Gunn-2019-ondansetron-5HT-mechanism-APT` | Gunn et al. 2019, *Aliment Pharmacol Ther* — mucosal 5-HT mechanism, super-responders, HTR3C genotype |

### MDMA pharmacology, immunology & trial safety
| File stem | Citation |
|---|---|
| `Connor-2004-MDMA-immune-stressor-Immunology` | Connor 2004, *Immunology* — MDMA as immune stressor (anti-inflammatory profile) |
| `Rojas-Fernandez-2014-serotonin-5HT3-antagonist` | Rojas-Fernandez 2014 — 5-HT3 antagonists & serotonin (rebuts serotonin-shunting) |
| `Meyer-2015-serotonin-syndrome-5HT3-APSF` | Meyer 2015, APSF Newsletter — serotonin syndrome w/ 5-HT3 antagonists, FDA action |
| `Mitchell-2023-MAPP2-MDMA-PTSD-phase3-NatureMedicine` | Mitchell et al. 2023, *Nature Medicine* — MAPP2 Phase 3 (Table 2 adverse events incl. muscle tightness) |
| `Colcott-2024-MDMA-side-effects-metaanalysis-Neuropsychopharm` | Colcott et al. 2024 — MDMA side-effects systematic review + meta-analysis (acute-only) |

### Bile acid ↔ serotonin / TGR5 / FXR crosstalk (the mechanistic core)
| File stem | Citation |
|---|---|
| `Alemi-2013-TGR5-EC-cell-5HT-CGRP-Gastroenterology` | Alemi et al. 2013, *Gastroenterology* — TGR5 on EC cells → 5-HT/CGRP → peristalsis (pro-motility arm) |
| `Poole-2010-TGR5-myenteric-neurons-NGM` | Poole et al. 2010, *Neurogastroenterol Motil* — TGR5 on nitrergic myenteric neurons (anti-motility arm) |
| `Kidd-2008-EC-cell-serotonin-bile-salts` | Kidd et al. 2008 — bile salts regulate EC-cell 5-HT release (normal vs neoplastic) |
| `Bunnett-2014-TGR5-neurohumoral-review-JPhysiol` | Bunnett 2014, *J Physiol* — TGR5 neuro-humoral signalling (senior-author synthesis of Alemi) |
| `Ticho-2019-bile-acid-receptors-GI-LiverRes` | Ticho et al. 2019, *Liver Res* — bile acid receptors & GI function (review) |
| `Joyce-OMalley-2022-bile-acids-gut-brain-JPhysiol` | Joyce & O'Malley 2022, *J Physiol* — bile acids in gut-to-brain interoceptive signalling |
| `Wei-Ghoshal-2022-EC-cell-microbiota-JNM` | Wei, Singh & Ghoshal 2022, *J Neurogastroenterol Motil* — EC cell–microbiota crosstalk |
| `Camilleri-2011-TGR5-variant-rs11554825-transit-NGM` | Camilleri et al. 2011, *Neurogastroenterol Motil* 23:995 — TGR5 SNP rs11554825 vs colonic transit (suggestive, borderline) |

---

## Notes for the meta-analysis (Fable) pass

- **Start from `bam-mdma-research-dossier.md`.** It already synthesizes across all 26 sources with
  tiers; the PDFs/extractions are there to verify or dig deeper on any specific claim.
- **The through-line to chase:** colesevelam measurably *raises* colonic **TGR5** expression
  (Vijayvargiya 2020); TGR5 has opposing pro-/anti-motility arms (Alemi 2013 vs Poole 2010); MDMA is
  serotonergic + anti-inflammatory (Connor 2004) and the owner's gut response is serotonin/TGR5-shaped.
  That TGR5 ↔ 5-HT ↔ inflammation triangle is where the novel hypothesis lives.
- **CRITICAL real-world protocol (Section 5):** the owner **never co-administers ondansetron and MDMA** —
  ondansetron is skipped entirely on any MDMA day, to avoid stacking serotonin-related drugs. So model
  the MDMA gut-response against a **colesevelam-only background (no 5-HT3 antagonist on board)**. The
  ondansetron↔MDMA interaction literature is retained for completeness but is moot for this individual.
- **Recurring pattern worth flagging:** in the drug RCTs (aldafermin, colesevelam) the *biochemistry*
  moves hard while *symptoms* barely move — a dissociation the meta-analysis should weight. The
  liraglutide/colesevelam companion (Ellegaard 2024) sharpens it: two effective drugs, *opposite*
  effects on where the bile acids end up (colesevelam → into stool; liraglutide → no fecal change).
- **Extractions are grep-friendly.** e.g. `grep -i "7αC4\|GPBAR1\|super-responder" docs/extractions/*.txt`.
- **Remaining Tier-2 sources not obtained in full text** (all paywalled; a free-copy hunt on
  2026-07-12 found no open version of any). Headline primary-endpoint numbers have been pulled from
  abstracts + trial coverage and added to the dossier at **CORROBORATED** tier (not VERIFIED):
  Borup 2023 (colesevelam Phase 4 RCT — n=168, 12 days), Kårhus 2022 (liraglutide RCT parent — n=52,
  6 wks; its BA-levels companion IS verified in `sources/`), Camilleri 2020 (tropifexor FXR RCT —
  target engagement but no stool-frequency change), Wei 2021 (human TGR5/IBS-D biopsy pilot — key
  finding already covered via Yang). Getting any to VERIFIED still needs the actual PDF.
