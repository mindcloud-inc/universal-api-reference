# Bria Generate Vector with CometAPI

Creates Bria vector graphics in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/bria/text-to-vector`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Bria Generate Vector](https://apidoc.cometapi.com/api/image/bria/generate-vector-graphics-base)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guidance_method_2_scale` | body | `number` | yes | Required Bria guidance scale. |
| `prompt` | body | `string` | yes | Text prompt for vector generation. |
