# Compress PDF with Formstack Documents

Compresses a PDF file in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/compress_pdf`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Compress PDF](https://www.webmerge.me/developers/tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file[contents]` | body | `string` | no | Base64-encoded PDF contents |
| `file[name]` | body | `string` | yes | Name of the PDF file to compress |
| `file[url]` | body | `string` | no | Remote URL for the PDF file to compress |
