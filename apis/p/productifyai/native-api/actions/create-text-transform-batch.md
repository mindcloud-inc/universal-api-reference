# Create Text Transform Batch with Productify.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/Batch/Transform`
- **Base URL:** `https://api.productify.ai`
- **Official documentation:** [Create Text Transform Batch](https://api.productify.ai/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transformInputs[]` | body | `array<object>` | yes | Text inputs to transform in the batch. |
