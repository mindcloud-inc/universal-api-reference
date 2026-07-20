# Replace Image Region with DeepAI

Creates an edited image by replacing a masked region in DeepAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/image-replace`
- **Base URL:** `https://api.deepai.org/api`
- **Official documentation:** [Replace Image Region](https://api.deepai.org/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The prompt describing what should replace the masked region. |
| `mask` | body | `string` | yes | The image URL or uploaded mask file identifying the region to replace. |
| `image` | body | `string` | yes | The source image URL or uploaded file to modify. |
