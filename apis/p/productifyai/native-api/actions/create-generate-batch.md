# Create Generate Batch with Productify.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/Batch/Generate`
- **Base URL:** `https://api.productify.ai`
- **Official documentation:** [Create Generate Batch](https://api.productify.ai/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products[]` | body | `array<object>` | yes | Products to process in the batch. |
