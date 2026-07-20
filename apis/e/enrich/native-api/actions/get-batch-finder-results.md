# Get Batch Finder Results with Enrich.so

Retrieves batch email finder results from Enrich.so.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-finder/batch/{batchId}/results`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Get Batch Finder Results](https://doc.enrich.so/get-batch-finder-results-27483198e0.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Batch ID returned by the batch email finder submit action. |
