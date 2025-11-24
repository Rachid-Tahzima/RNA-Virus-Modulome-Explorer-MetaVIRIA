# Modulome-Explorer
**The RNA Virus Modulome** is a conceptual web platform for organizing and exploring the modular architecture of proteins encoded by the realm **Riboviria**, using **UniProtKB** entries as the primary reference system. It deploys the MetaVIRIA Ai-driven algorithm to generate prediction for protein biophysical characterisation and host predictions.


# The RNA Virus Modulome & MetaVIRIA (Demo / Beta)

**Status:** Demo / Beta (front-end prototype only)

**The RNA Virus Modulome** is a conceptual web platform for organizing and exploring the modular architecture of proteins encoded by the realm **Riboviria**, using **UniProtKB** entries as the primary reference system.

The site includes a prototype AI/LLM-inspired component named **MetaVIRIA**, which illustrates how one might paste a protein sequence and obtain an *example* host prediction. In this demo, MetaVIRIA runs entirely in the browser using simple heuristic logic – it **does not** perform real machine learning or query UniProtKB.

---

## Key Components

- **Modulome Explorer (Demo)**
  - Mock table of conceptual Riboviria protein modules (e.g. RdRp, capsid, helicase, accessory).
  - Filterable by module class, status (reviewed/unreviewed), and text search.
  - Designed to be wired later to UniProtKB or an internal database.

- **MetaVIRIA – AI/LLM-based Host Prediction (Prototype)**
  - Small query window where users can paste a protein amino acid sequence.
  - “Predict Host” button runs simple, client-side motif-based heuristics.
  - Output includes an illustrative “predicted host class” and rationale.
  - **Not for clinical, diagnostic, or real scientific decision-making.**

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
https://YOUR_GITHUB_USERNAME.github.io/rna-virus-modulome/
