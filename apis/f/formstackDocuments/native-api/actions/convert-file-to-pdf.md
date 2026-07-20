# Convert File to PDF with Formstack Documents

Converts a file to PDF in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/convert_to_pdf`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Convert File to PDF](https://www.webmerge.me/developers/tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file[contents]` | body | `string` | no | Base64-encoded source file contents |
| `file[name]` | body | `string` | yes | Name of the source file to convert |
| `file[url]` | body | `string` | no | Remote URL for the source file |
