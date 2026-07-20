# Flatten Remote PDF with Nutrient Document Converter

Flattens a remote PDF in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Flatten Remote PDF](https://www.nutrient.io/guides/dws-processor/developer-guides/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdfUrl` | body | `string` | yes | Publicly reachable PDF URL. |
