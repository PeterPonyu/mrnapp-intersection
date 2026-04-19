<div align="center">
  <a href="https://peterponyu.github.io/">
    <img src="https://peterponyu.github.io/assets/badges/mrnapp-intersection.svg" width="64" alt="ZF Lab · mrnapp-intersection">
  </a>
</div>

# mRNA-seq Static Presentation Site

Public utility surface in the PeterPonyu public graph for browsing precomputed mRNA-seq analysis results.

## Public Graph Status

- This repository is a bounded static-export exception: it currently contains the rendered public export and supporting data/assets rather than the original application source tree.
- Homepage (`https://peterponyu.github.io/`) and SCPortal (`https://peterponyu.github.io/scportal/`) are the canonical discovery/root neighbors for this surface.
- The current public boundary is intentional. Future adapter work may replace the hardcoded shell links, but the explicit homepage and SCPortal linkage is correct for the current ecosystem contract.

## Scope

The site displays:
- Differential expression results per comparison
- GO Biological Process enrichment
- Gene search across all comparisons
- Intersection analysis across multiple comparisons

## Data Summary

- Organism: Mouse
- Comparisons: IRW_vs_CW, IR_vs_con, con_vs_CW, con_vs_IRW, IR_vs_CW, IR_vs_IRW
- Thresholds: |log2FC| >= 1.0, q-value <= 0.05

## Repository Shape

```
mrnapp-intersection/
├── index.html and route directories/  # Rendered static pages
├── _next/                             # Exported Next.js runtime assets
├── data/                              # Precomputed JSON data files
└── favicon.svg and metadata files     # Public-facing export assets
```

This checkout documents the deployed public surface as it exists today. Source-authoring and future adapter work, if reintroduced, should preserve the same public boundary unless the wider PeterPonyu graph contract changes.
