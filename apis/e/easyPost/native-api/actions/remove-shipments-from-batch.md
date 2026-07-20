# Remove Shipments From Batch with EasyPost

Removes shipments from an existing batch in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/batches/:id/remove_shipments`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Remove Shipments From Batch](https://docs.easypost.com/docs/batches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Batch ID, beginning with batch_. |
| `shipments[]` | body | `array<object>` | yes | Shipments to remove from the batch. |
