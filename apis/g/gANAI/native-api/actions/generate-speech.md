# Generate Speech with GAN.AI

Creates text-to-speech audio in GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tts`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Generate Speech](https://developer.gan.ai/api-reference/text-to-speech/tts-sync-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `voice_id` | body | `string` | yes |
