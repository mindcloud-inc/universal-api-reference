# Create Translation with Orq.ai

Creates an English audio translation in Orq.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/router/audio/translations`
- **Base URL:** `https://api.orq.ai`
- **Official documentation:** [Create Translation](https://docs.orq.ai/reference/audio/create-translation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `model` | body | `string` | yes |
