# Watermark Remote PDF with Nutrient Document Converter

Adds a watermark to a remote PDF in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Watermark Remote PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdfUrl` | body | `string` | yes | Publicly reachable PDF URL. |
| `text` | body | `string` | yes | Text to add as a watermark. |
| `opacity` | body | `number` | no | Watermark opacity from 0 to 1. |
