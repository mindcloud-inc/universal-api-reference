# Analyze Build Request with Nutrient Document Web Services

Analyzes a document build request in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/analyze_build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Analyze Build Request](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/analyze_build)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parts[]` | body | `array<object>` | yes | Source document parts. |
| `actions[]` | body | `array<object>` | no | Build actions to apply. |
| `output` | body | `object` | no | Output configuration. |
