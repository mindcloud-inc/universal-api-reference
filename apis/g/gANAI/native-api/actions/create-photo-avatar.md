# Create Photo Avatar with GAN.AI

Creates a photo avatar in GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/photo_avatars/create`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Create Photo Avatar](https://developer.gan.ai/api-reference/photo-avatars/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_image_url` | body | `string` | yes |
| `title` | body | `string` | no |
