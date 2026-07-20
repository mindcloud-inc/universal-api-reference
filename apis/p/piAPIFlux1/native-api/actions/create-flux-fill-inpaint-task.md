# Create Flux Fill Inpaint Task with PiAPI/Flux.1

Creates a Flux fill inpaint task in PiAPI/Flux.1.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Flux Fill Inpaint Task](https://piapi.ai/docs/flux-redux-fill-variation-inpaint-outpaint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.image` | body | `string` | yes |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
