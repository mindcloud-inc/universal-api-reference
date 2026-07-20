# Get Bulk Lookup Results with Enrich.so

Retrieves bulk profile lookup results from Enrich.so.

## Endpoint

- **Method:** `GET`
- **Path:** `/reverse-lookup/bulk-lookup/{batchId}/results`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Get Bulk Lookup Results](https://doc.enrich.so/get-bulk-lookup-results-27483206e0.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Bulk reverse lookup batch ID. |
