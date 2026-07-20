# Run Build Instructions with Nutrient Document Converter

Builds a document from custom instructions in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Run Build Instructions](https://www.nutrient.io/guides/dws-processor/developer-guides/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instructions` | body | `object` | yes | Complete Nutrient Build API instructions object. |
