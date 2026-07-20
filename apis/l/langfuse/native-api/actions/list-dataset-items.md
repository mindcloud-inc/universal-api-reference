# List Dataset Items with Langfuse

Retrieves dataset items from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/dataset-items`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Dataset Items](https://api.reference.langfuse.com/#tag/DatasetItems/GET/api/public/dataset-items)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datasetName` | query | `string` | no |
| `sourceObservationId` | query | `string` | no |
| `sourceTraceId` | query | `string` | no |
| `version` | query | `string` | no |
