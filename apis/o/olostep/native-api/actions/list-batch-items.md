# List Batch Items with Olostep

Retrieves items from an Olostep batch.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/batches/[:batch_id]/items`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [List Batch Items](https://docs.olostep.com/api-reference/batches/items)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | yes | The ID of the batch whose items you want to list. |
| `status` | query | `string` | no | Optional item status to retrieve from the batch. Accepted values: `0`, `1`. |
