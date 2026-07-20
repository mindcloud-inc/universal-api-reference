# Create Trellis Text-to-3D Task with PiAPI/Trellis

Creates a Trellis text-to-3D task in PiAPI/Trellis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Trellis Text-to-3D Task](https://piapi.ai/docs/trellis-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Prompt describing the 3D object to generate. |
| `input.seed` | body | `number` | no | Optional random seed. |
