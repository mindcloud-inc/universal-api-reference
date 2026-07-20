# Create Dataset with Langfuse

Creates a dataset in Langfuse.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/datasets`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Create Dataset](https://api.reference.langfuse.com/#tag/Datasets/POST/api/public/v2/datasets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `expectedOutputSchema` | body | `string` | no |
| `inputSchema` | body | `string` | no |
| `metadata` | body | `string` | no |
| `name` | body | `string` | no |
