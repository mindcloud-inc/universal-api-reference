# Create Prediction with BigML

Creates a prediction in BigML.

## Endpoint

- **Method:** `POST`
- **Path:** `/prediction`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Create Prediction](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | BigML model resource ID in full resource format (for example, model/69cd1234abcd1234abcd1234). |
| `input_data` | body | `object` | yes | Input field values as a JSON object keyed by field identifiers. |
