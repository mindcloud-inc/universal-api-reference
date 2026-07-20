# Create Dataset Item with Langfuse

Creates a dataset item in Langfuse.

## Endpoint

- **Method:** `POST`
- **Path:** `/dataset-items`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Create Dataset Item](https://api.reference.langfuse.com/#tag/DatasetItems/POST/api/public/dataset-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datasetName` | body | `string` | no |
| `expectedOutput` | body | `string` | no |
| `id` | body | `string` | no |
| `input` | body | `string` | no |
| `metadata` | body | `string` | no |
| `sourceObservationId` | body | `string` | no |
| `sourceTraceId` | body | `string` | no |
| `status` | body | `string` | no |
