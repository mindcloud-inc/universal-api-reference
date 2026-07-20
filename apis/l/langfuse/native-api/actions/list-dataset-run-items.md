# List Dataset Run Items with Langfuse

Retrieves dataset run items from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/dataset-run-items`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Dataset Run Items](https://api.reference.langfuse.com/#tag/DatasetRunItems/GET/api/public/dataset-run-items)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datasetId` | query | `string` | no |
| `runName` | query | `string` | no |
