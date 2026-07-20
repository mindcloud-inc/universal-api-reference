# Split PDF with 1001fx

Splits a PDF into individual pages in a ZIP file.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/splitpdf`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Split PDF](https://1001fx.com/functions/splitpdf)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `outputFormat` | body | `string` | no |
