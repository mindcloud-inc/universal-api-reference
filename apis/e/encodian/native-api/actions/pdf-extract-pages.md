# PDF Extract Pages with Encodian

Extracts PDF pages in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/ExtractPdfPages`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Extract Pages](https://support.encodian.com/hc/en-gb/articles/13958097048732)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | The file content of the source PDF file. |
| `StartPage` | body | `number` | no | Set the page number to begin extracting pages from. |
| `EndPage` | body | `number` | no | Set the page number to stop extracting pages on. |
| `PageNumbers` | body | `string` | no | A comma-separated list of page numbers to extract, for example 1,3,4. |
