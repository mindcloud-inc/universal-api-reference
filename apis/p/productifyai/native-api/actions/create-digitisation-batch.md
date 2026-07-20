# Create Digitisation Batch with Productify.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/Batch/Extract`
- **Base URL:** `https://api.productify.ai`
- **Official documentation:** [Create Digitisation Batch](https://api.productify.ai/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractInputs[]` | body | `array<object>` | yes | Image inputs to extract from in the batch. |
