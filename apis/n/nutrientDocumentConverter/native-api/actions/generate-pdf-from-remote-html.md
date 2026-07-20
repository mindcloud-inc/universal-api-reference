# Generate PDF from Remote HTML with Nutrient Document Converter

Generates a PDF from remote HTML in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Generate PDF from Remote HTML](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-generator-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `htmlUrl` | body | `string` | yes | Publicly reachable HTML file URL. |
