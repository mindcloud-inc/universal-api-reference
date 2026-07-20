# Create Dataset Run Item with Langfuse

Creates a dataset run item in Langfuse.

## Endpoint

- **Method:** `POST`
- **Path:** `/dataset-run-items`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Create Dataset Run Item](https://api.reference.langfuse.com/#tag/DatasetRunItems/POST/api/public/dataset-run-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdAt` | body | `string` | no |
| `datasetItemId` | body | `string` | no |
| `datasetVersion` | body | `string` | no |
| `metadata` | body | `string` | no |
| `observationId` | body | `string` | no |
| `runDescription` | body | `string` | no |
| `runName` | body | `string` | no |
| `traceId` | body | `string` | no |
