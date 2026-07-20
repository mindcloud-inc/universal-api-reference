# Flux Generate Image with CometAPI

Creates a Flux image in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/flux/v1/:model`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Flux Generate Image](https://apidoc.cometapi.com/api/image/flux/flux-generate-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Flux model identifier. |
| `prompt` | body | `string` | yes | Text prompt for image generation. |
