# Nabhae

Static site. Preview with `python3 -m http.server 8000`.

## Generate an optimized copy
Use Python 3.11+ and install Pillow, then run `python scripts/optimize-assets.py`. It refuses to overwrite an existing `optimized-site/`, externalizes embedded images to content-named WebP files, resizes to at most 1800×1800 and writes separate HTML. Source remains unchanged. Review compression fidelity and every section on mobile/desktop before deploying the entire output folder, not only its index.

The optimized binary/HTML output is not committed in this text-only PR. The generator is the reviewable change; producing a copy does not deploy it. No build service or runtime dependency is introduced on the static site.
