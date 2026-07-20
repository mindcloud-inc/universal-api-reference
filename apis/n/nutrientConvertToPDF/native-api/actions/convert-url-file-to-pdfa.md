# Convert URL File to PDF/A with Nutrient - Convert to PDF

Creates a PDF/A document from a file URL in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert URL File to PDF/A](https://www.nutrient.io/api/pdf-to-pdfa-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceUrl` | body | `string` | yes | URL of the file to convert to PDF/A. |
| `conformance` | body | `list` | yes | PDF/A conformance level for archival output. Accepted values: `PDF/A-1b`, `PDF/A-2a`, `PDF/A-2b`, `PDF/A-3b`. |
