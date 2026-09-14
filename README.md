# Women's Outfit Recommender — Advanced Catalog (Kaggle)

Extended outfit recommender for **large fashion catalogs** (hundreds/thousands of items per category). Uses CLIP embeddings with disk cache, top-K search, and flexible folder naming (`tshirt`/`tshirts`, `bag`/`bags`, etc.).

Includes the **`modified-woman-fit-categorey-images.zip`** sample dataset (~165 MB) as a [GitHub Release asset](https://github.com/mahsamb/women-outfit-recommender-advanced-kaggle/releases/latest).

Companion project:
- [women-outfit-recommender-kaggle](https://github.com/mahsamb/women-outfit-recommender-kaggle) — simpler baseline with the smaller `my_images` demo catalog

## Why this project

- **Large-catalog scaling** — precompute CLIP embeddings once, search top-K per category
- **Robust path detection** on Kaggle (classic and `/kaggle/input/datasets/<user>/<slug>` layouts)
- **Category aliases** — accepts `tshirt`, `bag`, `pants`, `shoes` folder names
- **Bundled advanced demo dataset** with many more products than the simple catalog

## Stack

`Python` · `PyTorch` · `Transformers (CLIP)` · `scikit-learn` · `OpenCV` · `ipywidgets` · `Kaggle`

## Dataset

| File | Description |
|------|-------------|
| [`modified-woman-fit-categorey-images.zip`](https://github.com/mahsamb/women-outfit-recommender-advanced-kaggle/releases/latest) | Demo catalog (~165 MB, GitHub Release) |

After unzip, layout is:

```
modified-woman-fit-categorey-images/   (or "Modified Woman Fit Categorey Images/")
├── tshirt/<product_id>/pic1.jpg
├── bag/<product_id>/pic1.jpg
├── pants/<product_id>/pic1.jpg
└── shoes/<product_id>/pic1.jpg
```

The notebook auto-extracts the zip on first local run if the folder is missing.

## Quick start

### Local / GitHub clone

1. Clone: `git clone https://github.com/mahsamb/women-outfit-recommender-advanced-kaggle.git`
2. Download [`modified-woman-fit-categorey-images.zip`](https://github.com/mahsamb/women-outfit-recommender-advanced-kaggle/releases/latest) into the repo folder.
3. Open [`women_outfit_recommender_advanced_kaggle_notebook.ipynb`](women_outfit_recommender_advanced_kaggle_notebook.ipynb).
4. Run all cells — section 3 auto-extracts the zip if the catalog folder is missing.
4. Set `REFERENCE_TSHIRT` or use the dropdown in section 4.

### Kaggle

1. Upload the notebook to [Kaggle](https://www.kaggle.com/code).
2. Add dataset [mahsamb/modified-woman-fit-categorey-images](https://www.kaggle.com/datasets/mahsamb/modified-woman-fit-categorey-images) via **Add Input**, **or** upload this repo's zip as your own Kaggle Dataset.
3. **Settings → Internet → ON**
4. Run all cells.

### Colab

Run section 3 — upload `modified-woman-fit-categorey-images.zip` when prompted.

## Model

| Component | Source |
|-----------|--------|
| **CLIP ViT-B/32** | [openai/clip-vit-base-patch32](https://huggingface.co/openai/clip-vit-base-patch32) (downloaded at runtime) |

## Disclaimer & third-party rights

- **Unofficial project** — independent notebook by Marzieh Babaali. **Not affiliated with OpenAI, Hugging Face, or any fashion retailer.**
- **CLIP weights** are downloaded at runtime from Hugging Face under the model's license.
- **Sample product images** in the bundled zip are a **demo catalog for research and education** to reproduce large-scale outfit recommendation. **Do not redistribute product photos for commercial use.** Use your own catalog where you hold usage rights.
- **Product IDs** are opaque identifiers from the demo collection, not endorsements of any brand or store.
- Notebook code in this repository is original MIT-licensed work ([LICENSE](LICENSE)).

## Author

**Marzieh Babaali** — PhD Researcher · NLP & Generative AI

- [Google Scholar](https://scholar.google.com/citations?user=eOcempcAAAAJ&hl=en)
- [LinkedIn](https://www.linkedin.com/in/marzieh-babaali-75934266)
- [GitHub](https://github.com/mahsamb)
