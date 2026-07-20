# Generate Flux Image with Apiframe

Creates a Flux image generation task in Apiframe.

## Endpoint

- **Method:** `POST`
- **Path:** `/flux-imagine`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Generate Flux Image](https://docs.apiframe.ai/flux/imagine)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `prompt` | body | `string` | yes |
