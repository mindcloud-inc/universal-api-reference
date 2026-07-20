# Merge PDF And XML with finaX

Creates a ZUGFeRD PDF by merging PDF and XML in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pdf/merge/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [Merge PDF And XML](https://docs.finax.dev/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdf_file` | body | `file` | yes | PDF file to merge. |
| `xml_file` | body | `file` | yes | XML file to merge. |
