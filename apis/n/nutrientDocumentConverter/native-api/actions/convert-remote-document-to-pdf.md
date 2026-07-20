# Convert Remote Document to PDF with Nutrient Document Converter

Converts a remote document to PDF in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert Remote Document to PDF](https://www.nutrient.io/guides/dws-processor/developer-guides/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentUrl` | body | `string` | yes | Publicly reachable source document URL. |
