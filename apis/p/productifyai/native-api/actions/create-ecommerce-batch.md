# Create Ecommerce Batch with Productify.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/Batch/Generate/Ecommerce`
- **Base URL:** `https://api.productify.ai`
- **Official documentation:** [Create Ecommerce Batch](https://api.productify.ai/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products[]` | body | `array<object>` | yes | Products to process in the batch. |
