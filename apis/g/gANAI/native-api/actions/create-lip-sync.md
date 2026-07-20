# Create LipSync with GAN.AI

Creates a lip-sync video in GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/lipsync/create_lipsync`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Create LipSync](https://developer.gan.ai/api-reference/lipsync/create-lipsync)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `inputs.input_audio_url` | body | `string` | yes |
| `inputs.input_video_url` | body | `string` | yes |
| `inputs.use_audio_from_video` | body | `boolean` | no |
| `title` | body | `string` | no |
