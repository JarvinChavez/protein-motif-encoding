# Protein Motif Encoding

NSF undergraduate research tooling — vectorize **UniProt motif regions** for downstream clustering and visualization work (related to [iCn3D integration](https://github.com/JarvinChavez/icn3d-implementation-proof-of-concept)).

---

## What it does

1. **`encode_motifs.py`** — Tokenize motif sequences into 2-character n-grams, build a vocabulary, and export a fixed-length numeric tensor (CSV).
2. **`select_grid.py`** — OpenCV UI to draw a bounding box and export normalized coordinates (used when mapping figure regions).
3. **`color_palette.py`** — Build a palette image from dominant RGB values in research figures.

---

## Run

```bash
pip install -r requirements.txt
python src/encode_motifs.py
python src/color_palette.py
python src/select_grid.py   # requires samples/example.png
```

---

## Data

| File | Description |
|------|-------------|
| `data/sample_motif_regions.csv` | Sample UniProt motif region rows |
| `data/encoded_motif_tensor.csv` | Generated after running encoder (optional output) |

---

## Stack

Python · pandas · NumPy · OpenCV · Pillow

---

## Author

**Jarvin Chavez** · [GitHub](https://github.com/JarvinChavez)
