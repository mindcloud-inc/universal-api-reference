# Create Photo Avatar with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/photo_avatar/photo/generate`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Create Photo Avatar](https://docs.jogg.ai/api-reference/v2/Avatar/PhotoAvatarGenerate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `age` | body | `string` | yes |
| `avatar_style` | body | `string` | yes |
| `gender` | body | `string` | yes |
| `model` | body | `string` | yes |
| `aspect_ratio` | body | `string` | yes |
| `ethnicity` | body | `string` | no |
| `background` | body | `string` | no |
| `appearance` | body | `string` | no |
| `image_url` | body | `string` | no |
