# Parse Document with PDF.co

Parses a document with PDF.co templates.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/documentparser`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Parse Document](https://docs.pdf.co/api-reference/documentparser/parser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the source PDF file to parse. |
| `templateid` | body | `string` | no | Optional pre-saved PDF.co template ID. |
| `template` | body | `string` | no | Inline parser template JSON. |
| `outputformat` | body | `string` | no | Optional output format (e.g. json, csv). |
| `generatecsvheaders` | body | `boolean` | no | Generate CSV headers when output format is csv. |
| `async` | body | `boolean` | no | Set true to run parsing as background job. |
| `name` | body | `string` | no | Optional output filename. |
