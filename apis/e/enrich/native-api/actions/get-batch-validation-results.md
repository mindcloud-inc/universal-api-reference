# Get Batch Validation Results with Enrich.so

Retrieves batch email validation results from Enrich.so.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-validation/batch/{batchId}/results`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Get Batch Validation Results](https://doc.enrich.so/get-batch-validation-results-27483194e0.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Batch ID returned by the batch validation submit action. |
