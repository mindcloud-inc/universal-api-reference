# Create Photo Avatar Inference with GAN.AI

Creates a talking-head video for a photo avatar in GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/photo_avatars/create_inference`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Create Photo Avatar Inference](https://developer.gan.ai/api-reference/photo-avatars/create-inference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `audio_url` | body | `string` | no |
| `photo_avatar_id` | body | `string` | yes |
| `text` | body | `string` | no |
| `title` | body | `string` | no |
| `voice_sample_url` | body | `string` | no |
