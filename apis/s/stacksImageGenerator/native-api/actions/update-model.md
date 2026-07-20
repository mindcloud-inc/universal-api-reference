# Update Model with 88stacks Image Generator

Updates an existing image generation model in 88stacks Image Generator.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/models/:id`
- **Base URL:** `https://api.88stacks.com`
- **Official documentation:** [Update Model](https://88stacks.com/docs/1.0/models/update.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the model to update. |
| `name` | body | `string` | no | New name for the model. |
| `callback` | body | `string` | no | Webhook URL to call for model updates. |
