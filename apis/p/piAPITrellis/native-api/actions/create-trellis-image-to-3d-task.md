# Create Trellis Image-to-3D Task with PiAPI/Trellis

Creates a Trellis image-to-3D task in PiAPI/Trellis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Trellis Image-to-3D Task](https://piapi.ai/docs/trellis-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | no | Prompt describing the desired 3D object. |
| `input.images[]` | body | `array<string>` | yes | One or more source image URLs. Send multiple values as a array. |
