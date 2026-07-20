# Bulk Download Original Documents with DocuPipe

Creates bulk original document download URLs in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/download/bulk-original-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Bulk Download Original Documents](https://docs.docupipe.ai/reference/bulk_original_download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to download as original files. |
