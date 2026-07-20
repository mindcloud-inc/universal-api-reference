# Remix Ideogram Image with Apiframe

Creates an Ideogram remix task in Apiframe.

## Endpoint

- **Method:** `POST`
- **Path:** `/ideogram-remix`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Remix Ideogram Image](https://docs.apiframe.ai/ideogram/remix)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `image_url` | body | `string` | yes |
| `prompt` | body | `string` | yes |
| `image_weight` | body | `number` | yes |
