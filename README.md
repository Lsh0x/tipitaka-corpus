# Tipitaka Corpus

Hosts the corpus DBs and version manifests for the [Tipitaka iOS app](https://github.com/Lsh0x/tipitaka).

## Files

- `corpus_manifest_prod.json` — production manifest, fetched at runtime
- `corpus_manifest_staging.json` — staging manifest

## Releases

Corpus DBs are attached as release assets, tagged `corpus-YYYY-MM-DD`.
Each release contains:

- `corpus_en.db` — English (Sujato, Bodhi)
- `corpus_fr.db` — Français (Wijayaratna, Christelle, Maes)
- `corpus_vi.db` — Tiếng Việt (Thích Minh Châu)

Why this repo: the app's main source repo is private. Public hosting
here means anyone can download the corpus without auth, and GitHub's
edge network is reachable from regions where Drive isn't.
