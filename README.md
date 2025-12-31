# Examples

This repository contains **practical, end-to-end machine learning examples** for **MLArtisan**, focused on **real API usage**.

Each example shows how to go from **raw data → schema → dataset → model → prediction**, using ready-made API request bodies.

🔗 MLArtisan: [https://mlartisan.com/](https://mlartisan.com/)

---

## Repository description

**Examples** is a collection of real-world ML scenarios implemented as reproducible examples for MLArtisan.

The goal is to help developers understand:

* how MLArtisan API is used step by step
* how data, schema, and models are connected
* how the same flow works via **API** and **UI**

---

## What is inside

Each folder represents **one complete ML scenario** (for example: churn prediction, anomaly detection, user segmentation).

Inside every example you will find:

* a dataset used in the scenario
* JSON files with **ready-to-use API request bodies**
* a clear, repeatable sequence of steps

No ML background is required — examples focus on **integration**, not theory.

---

## Repository structure

```
Examples/
│
├── Telco-Customer-Churn/
│   ├── Dataset.csv
│   ├── Schema.json
│   ├── Dataset.json
│   ├── Train.json
│   ├── Run.json
│   └── README.md
```

---

## Files explained

Each example contains the following files:

* **Dataset.csv**
  The processed dataset used for the example.

* **Schema.json**
  API request body for creating a schema in MLArtisan
  (features, types, target column, task type).

* **Dataset.json**
  API request body for attaching the normalized version of `dataset.csv` to a schema
  (uses `schemaId`).

* **Train.json**
  API request body for training a model
  (uses `schemaId`).

* **Run.json**
  API request body for running the trained model
  (prediction request).

All JSON files can be used **as-is** with MLArtisan API.

---

## How to use

### Option A — API usage (recommended)

Follow these steps in order:

1. **Create schema**
   Use `Schema.json` as the request body.

2. **Add dataset to schema**
   Use `Dataset.json` as the request body
   (replace `schemaId` with the value returned from step 1).

3. **Train model**
   Use `Train.json` as the request body
   (replace `schemaId`).

4. **Run model**
   Use `Run.json` to get predictions.

Each example folder follows the same flow.

---

### Option B — UI usage

You can reproduce the same steps using the MLArtisan UI:

1. Create a **Schema**
   Use fields and settings from `Schema.json`.

2. Upload **Dataset**
   Select the created schema and use Data from `Dataset.json`.

3. Create and **Train Model**
   Configure training options using `Train.json`.

4. **Run Model**
   Provide input data based on `Run.json`.

The JSON files serve as a **reference configuration** for the UI.

---

## Steps summary

```
Create schema
   ↓
Add dataset to schema
   ↓
Train model
   ↓
Run model
```

This flow is identical for all examples in this repository.

---

## Feedback and ideas

If you have:

* ideas for new examples
* questions about API usage
* real-world problems you want to solve with MLArtisan

Feel free to open an issue, start a discussion, or contact me directly:

📧 [contact@mlartisan.com](mailto:contact@mlartisan.com)

---

## Notes

* Examples are designed for **educational and demo purposes**
* Original datasets come from public sources
* Always review dataset licenses before production use
