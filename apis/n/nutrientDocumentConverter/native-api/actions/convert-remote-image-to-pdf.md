# Convert Remote Image to PDF with Nutrient Document Converter

Converts a remote image to PDF in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert Remote Image to PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/image-to-pdf-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrl` | body | `string` | yes | Publicly reachable image URL. |
