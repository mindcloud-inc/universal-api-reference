# Detect AI Image with Winston AI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/image-detection`
- **Base URL:** `https://api.gowinston.ai`
- **Official documentation:** [Detect AI Image](https://docs.gowinston.ai/api-reference/v2/image-detection/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public image URL to scan for AI generation signals. |
| `version` | body | `string` | no | The Winston AI image model version to use. |
