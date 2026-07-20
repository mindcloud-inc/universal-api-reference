# Edit Image with DeepAI

Creates an edited image from a prompt in DeepAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/image-editor`
- **Base URL:** `https://api.deepai.org/api`
- **Official documentation:** [Edit Image](https://api.deepai.org/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | The image URL or uploaded file to edit. |
| `text` | body | `string` | yes | The editing instruction describing how to change the image. |
