# Convert URL File to PDF with Nutrient - Convert to PDF

Creates a PDF document from a file URL in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert URL File to PDF](https://www.nutrient.io/api/url-to-pdf-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceUrl` | body | `string` | yes | URL of the file to download and convert to PDF. |
