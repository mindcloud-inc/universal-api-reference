# Split PDF with Formstack Documents

Splits a PDF file in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/split_pdf`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Split PDF](https://www.webmerge.me/developers/tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extract` | body | `string` | no | Page ranges to extract |
| `file[contents]` | body | `string` | no | Base64-encoded PDF contents |
| `file[name]` | body | `string` | yes | Name of the PDF file to split |
| `file[url]` | body | `string` | no | Remote URL for the PDF file to split |
| `remove` | body | `string` | no | Page ranges to remove |
