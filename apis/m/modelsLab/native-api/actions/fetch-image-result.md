# Fetch Image Result with ModelsLab

Retrieves a generated image result from ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/images/fetch/{request_id}`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Fetch Image Result](https://docs.modelslab.com/image-generation/realtime-stable-diffusion/fetchimage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | no | Image generation request ID returned by a generation action. |
