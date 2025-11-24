# Modulome-Explorer & MetaVIRIA
**The RNA Virus Modulome** is a conceptual web platform for organizing and exploring the modular architecture of proteins encoded by the realm **Riboviria**, using **UniProtKB** entries as the primary reference system. It deploys the MetaVIRIA Ai-driven algorithm to generate prediction for protein biophysical characterisation and host predictions.

Recent breakthroughs in protein structure prediction have generated a vast landscape of high-quality 3D models, necessitating scalable and biologically interpretable methods for navigating and exploiting this rapidly expanding protein universe. MetaVIRIA is a protein-centered, modular structural bioinformatics framework that unifies geometric motif detection, low-dimensional structural embeddings, intrinsic disorder modeling, and sequence-derived energetic profiling to decode RNA–protein biophysical determinants of viral host range and transmission. By integrating structural clusters from diverse large-scale protein structure collections into a single cohesive low-dimensional representation, MetaVIRIA reveals that proteins from distinct databases occupy separate yet functionally overlapping regions of structural space, reflecting a shared landscape of high-level biological functions. Mapping functional annotations, disorder-mediated dynamics, and RNA-interaction signatures onto this unified protein structure space enables the delineation of conserved structural determinants across viral and host proteomes.
MetaVIRIA’s structure- and intrinsic-disorder–based Modulome quantifies a suite of novel biophysical properties—including solvent-accessibility patterns, charge and protonation states, conformational plasticity, energy-profile signatures, and residue-level spatial networks. These features, embedded jointly with geometric motifs and rarity-weighted interaction patterns, allow sensitive detection of discontinuous or weakly conserved RNA-binding modules even within highly divergent viral proteins. A sequence-informed energetic model, strongly correlated with structure-derived energy landscapes, supports rapid comparative analysis across millions of proteins and enhances the interpretability of inferred sequence–structure–function relationships.
By training predictive models on these Modulome-derived biophysical signatures, MetaVIRIA identifies protein-level determinants distinguishing direct-contact, environmental, and vector-borne viral transmission pathways across animal, plant, and human viruses. This unified, scalable representation of protein structure space—paired with an interactive exploration platform—enables new biological questions to be asked about taxonomic origin, ecological context, and functional specificity, providing a generalizable foundation for discovery-driven research across global virome and host proteome datasets




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
