# Create Model with BigML

Creates a model in BigML.

## Endpoint

- **Method:** `POST`
- **Path:** `/model`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Create Model](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | body | `string` | yes | BigML dataset resource ID in full resource format (for example, dataset/69cd1234abcd1234abcd1234). |
| `objective_field` | body | `string` | no | Optional dataset field identifier to predict. If omitted, BigML chooses the objective field automatically. |
