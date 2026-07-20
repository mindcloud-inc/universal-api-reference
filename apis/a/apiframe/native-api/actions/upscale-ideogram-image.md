# Upscale Ideogram Image with Apiframe

Creates an Ideogram image upscale task in Apiframe.

## Endpoint

- **Method:** `POST`
- **Path:** `/ideogram-upscale`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Upscale Ideogram Image](https://docs.apiframe.ai/ideogram/upscale)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `image_url` | body | `string` | yes |
| `prompt` | body | `string` | yes |
| `resemblance` | body | `number` | yes |
