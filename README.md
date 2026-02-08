# mRNA-seq Static Presentation Site

Static web site for browsing precomputed mRNA-seq analysis results. The site is built with Next.js static export and is deployed to GitHub Pages.

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

## Project Layout

```
mrnaseq-static-site/
├── public/data/              # Precomputed JSON data files
│   ├── metadata.json
│   ├── differential/
│   ├── enrichment/
│   ├── gene-expression/
│   ├── gene-search/
│   └── intersection/
├── scripts/                  # Data generation scripts
├── src/                      # Next.js app
└── .github/workflows/        # GitHub Actions deployment
```

## Build

```
npm install
npm run build
```

The static output is written to `out/`.

## Deployment

The GitHub Actions workflow in `.github/workflows/deploy.yml` deploys the static output to GitHub Pages on pushes to `main`.

If the repository name changes, update `basePath` and `assetPrefix` in `next.config.js`.