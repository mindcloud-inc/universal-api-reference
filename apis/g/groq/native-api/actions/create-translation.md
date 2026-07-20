# Create Translation with Groq

Creates an audio translation in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/audio/translations`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Translation](https://console.groq.com/docs/api-reference#audio-translation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | no |
| `url` | body | `string` | no |
| `model` | body | `string` | yes |
| `prompt` | body | `string` | no |
| `response_format` | body | `list` | no |
| `temperature` | body | `number` | no |
