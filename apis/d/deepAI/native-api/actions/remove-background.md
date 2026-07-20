# Remove Background with DeepAI

Creates an image with the background removed in DeepAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/background-remover`
- **Base URL:** `https://api.deepai.org/api`
- **Official documentation:** [Remove Background](https://api.deepai.org/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | The image URL or uploaded file to process. |
