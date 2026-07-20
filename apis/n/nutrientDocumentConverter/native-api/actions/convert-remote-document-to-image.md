# Convert Remote Document to Image with Nutrient Document Converter

Converts a remote document to images in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert Remote Document to Image](https://www.nutrient.io/guides/dws-processor/tools-and-api/document-to-image-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentUrl` | body | `string` | yes | Publicly reachable source document URL. |
| `format` | body | `string` | no | Image format to output. |
| `width` | body | `number` | no | Optional output width in pixels. |
