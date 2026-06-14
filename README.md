# Protein Motif Encoding

NSF undergraduate research — vectorize **UniProt motif regions** into fixed-length numeric tensors for unsupervised clustering and bioinformatics analysis.

Related visualization work: [iCn3D integration](https://github.com/JarvinChavez/icn3d-implementation-proof-of-concept) · separate figure tooling in [color-recognition](https://github.com/JarvinChavez/color-recognition)

---

## What it does

`encode_motifs.py` reads motif region sequences from CSV, tokenizes them into 2-character n-grams (skipping gap characters `.`), builds a vocabulary, and exports a numeric matrix suitable for scikit-learn / clustering pipelines.

This matches the **Protein Motif Clustering Pipeline** work on my resume — encoding step before clustering hundreds of thousands of UniProt proteins.

---

## Run

```bash
pip install -r requirements.txt
python src/encode_motifs.py
```

Output: `data/encoded_motif_tensor.csv`

---

## Data

| File | Description |
|------|-------------|
| `data/sample_motif_regions.csv` | Sample UniProt rows with motif region sequences |
| `data/encoded_motif_tensor.csv` | Generated tensor (created by script) |

---

## Stack

Python · pandas · NumPy

---

## Author

**Jarvin Chavez** · [GitHub](https://github.com/JarvinChavez)
