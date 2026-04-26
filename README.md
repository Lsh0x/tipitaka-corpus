# Tipitaka Corpus

Hosts the corpus DBs and version manifests for the [Tipitaka iOS app](https://github.com/Lsh0x/tipitaka).

## Layout

```
prod/
  corpus_manifest.json     production manifest
staging/
  corpus_manifest.json     staging manifest (newer DBs in test)
```

The app fetches the manifest at runtime, picks the right environment via
the `MANIFEST_URL` build flag (see `dart_defines/{prod,staging}.json` in
the app repo), then downloads the corpus DBs referenced by the manifest.

## Releases

Corpus DBs are attached as release assets, tagged `corpus-YYYY-MM-DD`
(or `corpus-staging-...` / `corpus-prod-...` once the two diverge).
Each release contains:

- `corpus_en.db` — English (Sujato, Bodhi)
- `corpus_fr.db` — Français (Wijayaratna, Christelle, Maes)
- `corpus_vi.db` — Tiếng Việt (Thích Minh Châu)

## Why this repo

The app's main source repo is private. Public hosting here means anyone
can fetch the manifest + corpus without auth, and GitHub's edge network
is reachable from regions where Drive isn't.
