# Add Voice with GAN.AI

Creates a custom voice in GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voices`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Add Voice](https://developer.gan.ai/api-reference/voices/add-voice)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `voice_description` | body | `string` | no |
| `voice_name` | body | `string` | no |
