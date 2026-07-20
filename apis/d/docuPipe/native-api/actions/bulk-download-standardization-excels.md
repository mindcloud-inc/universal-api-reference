# Bulk Download Standardization Excels with DocuPipe

Creates bulk Excel download URLs for DocuPipe standardizations.

## Endpoint

- **Method:** `POST`
- **Path:** `/standardization/download/bulk-excel`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Bulk Download Standardization Excels](https://docs.docupipe.ai/reference/bulk_excel_download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `standardizationIds[]` | body | `array<string>` | yes | List of standardization IDs to download as Excel files. |
