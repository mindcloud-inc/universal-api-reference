# Create Trellis2 Image-to-3D Task with PiAPI/Trellis

Creates a Trellis2 image-to-3D task in PiAPI/Trellis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Trellis2 Image-to-3D Task](https://piapi.ai/docs/trellis2-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image` | body | `string` | yes | Source image URL. |
| `input.seed` | body | `number` | no | Optional random seed. |
