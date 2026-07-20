# Merge Documents with PDF Blocks

Creates a merged PDF document in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/merge_documents`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Merge Documents](https://www.pdfblocks.com/docs/api/merge-pdf-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file[]` | body | `array<file>` | yes | The PDF documents to merge, in order. |
