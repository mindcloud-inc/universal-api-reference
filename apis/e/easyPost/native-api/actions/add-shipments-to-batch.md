# Add Shipments To Batch with EasyPost

Adds shipments to an existing batch in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/batches/:id/add_shipments`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Add Shipments To Batch](https://docs.easypost.com/docs/batches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Batch ID, beginning with batch_. |
| `shipments[]` | body | `array<object>` | yes | Shipments to add to the batch. |
