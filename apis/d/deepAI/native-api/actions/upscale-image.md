# Upscale Image with DeepAI

Creates a sharper, upscaled image in DeepAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/torch-srgan`
- **Base URL:** `https://api.deepai.org/api`
- **Official documentation:** [Upscale Image](https://api.deepai.org/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | The image URL or uploaded file to upscale. |
