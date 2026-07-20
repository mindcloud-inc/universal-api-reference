# Bulk Download Original Documents with DocuPanda - Document Understanding

Creates a bulk original document download URL in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/download/bulk-original-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Bulk Download Original Documents](https://docs.docupipe.ai/reference/bulk_original_download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | body | `list<string>` | yes | List of document IDs to download as original files. |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to download as original files. |
