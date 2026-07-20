# Create IP Batch Export with Opportify

Creates an export job for IP batch results in Opportify.

## Endpoint

- **Method:** `POST`
- **Path:** `/ip/batch/:jobId/exports`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Create IP Batch Export](https://www.opportify.ai/docs/api/api-reference/create-ip-batch-export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The unique identifier of the completed batch job. Format: uuid. Example: "52b36b1f-0c21-41fa-8a4f-423d25a9a8e2". |
| `exportType` | body | `string` | no | Output format for the export. If omitted, the server will use `csv` as the default format. Allowed values: `csv`, `json`. Example: `csv`. |
| `filters` | body | `object` | no | Field-level filters to apply to the export. Supports string filters (exact match, comma-separated, or arrays), numeric filters (exact values, arrays, or range objects with min/max), and nested field access using dot notation.  - Maximum 25 filters - Maximum 50 values per filter |
| `columns[]` | body | `array<string>` | no | Array of field paths to include in the export. If omitted, all fields are included. Maximum 100 columns. |
