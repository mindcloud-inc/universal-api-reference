# Create Batch with Omnisend

Creates a batch request in Omnisend.

## Endpoint

- **Method:** `POST`
- **Path:** `/v5/batches`
- **Base URL:** `https://api.omnisend.com`
- **Official documentation:** [Create Batch](https://api-docs.omnisend.com/reference/post_batches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint` | body | `string` | yes | Use the Omnisend resource token, not a path. Verified values include contacts, products, categories, and events. |
| `items[]` | body | `array<object>` | yes | — |
| `method` | body | `string` | yes | — |
