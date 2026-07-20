# List Dataset Runs with Langfuse

Retrieves dataset runs from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasets/:datasetName/runs`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Dataset Runs](https://api.reference.langfuse.com/#tag/Datasets/GET/api/public/datasets/{datasetName}/runs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datasetName` | path | `string` | no |
