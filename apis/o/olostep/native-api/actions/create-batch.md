# Create Batch with Olostep

Creates a new batch in Olostep.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batches`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Create Batch](https://docs.olostep.com/api-reference/batches/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | yes | Array of batch items to process. Each item should include at least a URL and can optionally include a custom_id. |
