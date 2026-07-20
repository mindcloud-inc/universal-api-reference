# Generate Virtual Try-On with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Virtual Try-On](https://piapi.ai/docs/kling-api/virtual-try-on-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.model_input` | body | `string` | yes | Model or person image URL for the try-on request. |
| `input.upper_input` | body | `string` | no | Upper garment image URL. |
| `input.lower_input` | body | `string` | no | Lower garment image URL. |
| `input.batch_size` | body | `number` | no | Number of try-on outputs to generate. PiAPI accepts values from 1 to 4. |
