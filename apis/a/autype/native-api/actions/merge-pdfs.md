# Merge PDFs with Autype

Creates a PDF merge job in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/pdf/merge`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Merge PDFs](https://docs.autype.com/api-reference/developer-api/merge-pdfs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileIds[]` | body | `array<string>` | yes |
