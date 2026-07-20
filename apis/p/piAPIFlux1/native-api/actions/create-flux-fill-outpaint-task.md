# Create Flux Fill Outpaint Task with PiAPI/Flux.1

Creates a Flux fill outpaint task in PiAPI/Flux.1.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Flux Fill Outpaint Task](https://piapi.ai/docs/flux-redux-fill-variation-inpaint-outpaint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.image` | body | `string` | yes |
| `input.custom_settings[]` | body | `array` | yes |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
