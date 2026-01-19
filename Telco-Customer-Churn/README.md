# Customer Churn — Example

This example demonstrates how **customer churn prediction** can be implemented using **MLArtisan**, from raw data to model execution.

The folder contains both the **original dataset** and its **normalized representation** used for API requests.

---

## Files overview

* **dataset.csv**
  Original dataset in human-readable form
  (categorical values, strings, raw numbers).

* **dataset.json**
  Normalized version of `dataset.csv`, represented as JSON and used directly in MLArtisan API requests.

* **schema.json**
  Schema definition describing features, types, and target column.

* **train.json**
  Model training request body.

* **run.json**
  Model execution (prediction) request body.

---

## How to use this example with MLArtisan

### API usage

Follow these steps in order:

1. **Create schema**
   Use `schema.json` as request body.

2. **Add dataset**
   Use `dataset.json` as request body (normalized values).
   Replace `schemaId` with the ID returned from step 1.

3. **Train model**
   Use `train.json` (replace `schemaId`).

4. **Run model**
   Use `run.json` to get predictions.

---

### UI usage

You can reproduce the same configuration using the MLArtisan UI:

1. Create a schema using fields from `schema.json`
2. Upload data using fields from `dataset.json`
3. Configure training options based on `train.json`
4. Run predictions using values from `run.json`

---

## Notes

* Normalization logic is specific to this example
* Different examples may use different encoding strategies
* Examples of all transformations are documented for transparency and reproducibility

---

## Feedback

If you have questions about this example or ideas for improvements, feel free to open an issue or contact:

📧 [contact@mlartisan.com](mailto:contact@mlartisan.com)
