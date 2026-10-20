# imazen-26-originals

imazen-26 is a corpus for testing image codecs and image processing.

This repository holds the source files byte for byte. It includes JPEG, PNG,
HEIC and DNG; their encoded metadata and orientation remain in the files.

Version 2026.10.19: 2109 images,
2109 files, 4838631909 encoded bytes.

| branch | images | files | bytes |
|---|---:|---:|---:|
| `train` | 1064 | 1064 | 2437158772 |
| `validate` | 644 | 644 | 1487839541 |
| `test` | 401 | 401 | 913633596 |

`main` contains documentation. Each data branch contains only its own bucket.
Related sources and all renditions share a bucket. Do not train or tune on
`validate` or `test`; keep both out of fitting and default selection.

```sh
git clone --branch train --single-branch --depth 1 https://github.com/imazen/imazen-26-originals.git
```

See [DECODING.md](DECODING.md) for decoder commands, colour/HDR handling and hashes.

`manifest.tsv` identifies each file, its bucket, encoded SHA-256, licence and
source provenance. The image licences differ; the Unsplash files retain the
[Unsplash License](https://unsplash.com/license), while the other files are
public domain or CC0 as specified per row. `provenance_json` preserves attribution
and source URLs. The corpus tooling's software licence does not replace these licences.

Layers: originals (2109).

Source and validation: [imazen-26](https://github.com/imazen/imazen-26).
