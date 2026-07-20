# Create Translation with Open AI

Translates audio into English in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/audio/translations`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Translation](https://developers.openai.com/api/reference/resources/audio/subresources/translations/methods/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Audio file input for translation. |
| `model` | body | `list` | yes | Translation model ID. |
