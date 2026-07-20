# Build Document with Nutrient Document Web Services

Creates a processed document in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Build Document](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/build-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parts[]` | body | `array<object>` | yes | Source document parts. |
| `actions[]` | body | `array<object>` | no | Build actions to apply. |
| `output` | body | `object` | no | Output configuration. |
