# Create Email Batch Export with Opportify

Creates an export job for email batch results in Opportify.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/batch/:jobId/exports`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Create Email Batch Export](https://www.opportify.ai/docs/api/api-reference/create-email-batch-export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The unique identifier of the completed batch job. Format: uuid. Example: "84d22c8b-2cb6-4606-bfb1-361244a097e4". |
| `exportType` | body | `string` | no | Output format for the export. If omitted, the server will use `csv` as the default format. Allowed values: `csv`, `json`. Example: `csv`. |
| `filters` | body | `object` | no | Field-level filters to apply to the export. Supports string filters (exact match, comma-separated, or arrays), numeric filters (exact values, arrays, or range objects with min/max), and nested field access using dot notation.  - Maximum 25 filters - Maximum 50 values per filter |
| `columns[]` | body | `array<string>` | no | Array of field paths to include in the export. If omitted, all fields are included. Maximum 100 columns. |
