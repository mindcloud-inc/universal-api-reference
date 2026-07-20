# Buy Batch with EasyPost

Purchases an existing batch in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/batches/:id/buy`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Buy Batch](https://docs.easypost.com/docs/batches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Batch ID, beginning with batch_. |
