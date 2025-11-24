# Modulome-Explorer & MetaVIRIA
**The RNA Virus Modulome** is a conceptual web platform for organizing and exploring the modular architecture of proteins encoded by the realm **Riboviria**, using **UniProtKB** entries as the primary reference system. It deploys the MetaVIRIA Ai-driven algorithm to generate prediction for protein biophysical characterisation and host predictions.


Explosive growth in high-quality protein structure prediction has opened new opportunities for decoding how RNA–protein biophysical features shape viral ecology, yet it has also magnified the need for unified, scalable methods capable of interpreting massive and heterogeneous structural datasets. MetaVIRIA is a modular structural bioinformatics pipeline that leverages geometrical motif discovery, low-dimensional structural embeddings, intrinsic disorder analysis, and sequence-derived energetic modeling to characterize RNA-binding proteins and infer viral host range and transmission modes. By integrating 3D structural motifs, disorder-aware residue features, and position-independent geometric signatures into a cohesive protein structure space, MetaVIRIA captures conserved RNA-interaction determinants that underpin host specificity across diverse viral clades. A sequence-informed energy model—highly correlated with structure-based energetics—enables rapid comparison across millions of viral and host proteins, while a rarity-weighted structural motif index sensitively detects discontinuous or weakly conserved RNA-binding patterns in highly divergent proteomes.
Central to MetaVIRIA is its structure- and intrinsic-disorder–based Modulome, which quantifies novel biophysical properties including solvent accessibility dynamics, charge and protonation landscapes, disorder-mediated conformational plasticity, and residue-level proximity networks. These biophysical modules are jointly embedded into the structural space to produce interpretable functional signatures. By training its predictive models on these Modulome-derived features, MetaVIRIA uncovers the structural and energetic determinants that differentiate direct-contact, environmental, and vector-borne viral transmission pathways across animal, plant, and human viruses.
Together, this integrative framework provides fast, scalable, and biologically interpretable predictions of viral host range and transmission mode, while enabling discovery-oriented exploration of sequence–structure–function relationships across global virome datasets.


# The RNA Virus Modulome & MetaVIRIA (Beta_v1)

**Status:** Beta_v1 / front-end prototype

**The RNA Virus Modulome** is a conceptual web platform for organizing and exploring the modular architecture of proteins encoded by the realm **Riboviria**, using **UniProtKB** entries as the primary reference system.

The site includes a prototype AI/LLM-inspired component named **MetaVIRIA**, which illustrates how one might paste a protein sequence and obtain an *example* host prediction. In this demo, MetaVIRIA runs entirely in the browser using simple heuristic logic – it **does not** perform real machine learning or query UniProtKB.

---

## Key Components

- **Modulome Explorer (Demo)**
  - Mock table of conceptual Riboviria protein modules (e.g. RdRp, capsid, helicase, siRNA Silencing, Movement Proteinsaccessory).
  - Filterable by module class, status (reviewed/unreviewed), and text search.
  - Designed to be wired later to UniProtKB or an internal database.

- **MetaVIRIA – AI/LLM-based Host Prediction (Prototype)**
  - Small query window where users can paste a protein amino acid sequence.
  - “Predict Host” button runs simple, client-side motif-based heuristics.
  - Output includes an illustrative “predicted host class” and rationale.
  - **Not for clinical, diagnostic decision-making.**

- **Data Source (Conceptual)**
  - Inspired by the UniProtKB search for “Riboviria”:
    - https://www.uniprot.org/uniprotkb?query=Riboviria
  - A production deployment must:
    - Respect UniProt licenses and terms of use.
    - Implement proper caching, rate limiting, and attribution.
    - Regularly synchronize with updated UniProtKB entries.

- **Main Webmaster & Designer**
  - **Prof. Dr. ir. Rachid TAHZIMA**
  - Responsible for the conceptual architecture, visual identity,
    and scientific positioning of *The RNA Virus Modulome* and *MetaVIRIA*.

---

## Live Demo / Deployment

This repo is intended to be deployed as a static site with a single `index.html`.

### GitHub Pages (recommended for demo)

1. Commit `index.html` to the root of this repository.
2. Go to **Settings → Pages**.
3. Under **Source**, choose:
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
4. Click **Save**.

After a short build, GitHub Pages will provide a URL:

```text
https://github.io/rna-virus-modulome/
