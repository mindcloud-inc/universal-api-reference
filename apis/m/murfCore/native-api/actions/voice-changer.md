# Voice Changer with Murf Core

Converts audio to another voice with Murf Core.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice-changer/convert`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [Voice Changer](https://murf.ai/api/docs/api-reference/voice-changer/convert)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_id` | body | `string` | yes | Target Murf voice ID for the converted audio. |
| `file` | body | `file` | no | Audio file to convert. |
| `file_url` | body | `string` | no | Public URL for the source audio file. |
| `format` | body | `string` | no | Output audio format. |
| `encode_output_as_base64` | body | `boolean` | no | Return the generated audio as base64 in the response. |
| `channel_type` | body | `string` | no | Output channel type. |
| `sample_rate` | body | `number` | no | Output sample rate in hertz. |
