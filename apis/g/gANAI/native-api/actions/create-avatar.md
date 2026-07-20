# Create Avatar with GAN.AI

Creates an avatar in GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/avatars/create_avatar`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Create Avatar](https://developer.gan.ai/api-reference/avatars/create-avatar)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_video_url` | body | `string` | yes |
| `title` | body | `string` | no |
