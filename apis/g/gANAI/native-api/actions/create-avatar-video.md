# Create Avatar Video with GAN.AI

Creates an avatar video in GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/avatars/create_video`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Create Avatar Video](https://developer.gan.ai/api-reference/avatars/create-video)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `audio_url` | body | `string` | no |
| `avatar_id` | body | `string` | yes |
| `text` | body | `string` | no |
| `title` | body | `string` | no |
