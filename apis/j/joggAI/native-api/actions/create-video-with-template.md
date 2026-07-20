# Create Video with Template with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/create_video_with_template`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Create Video with Template](https://docs.jogg.ai/api-reference/v2/Video/CreateVideoWithTemplate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | body | `number` | yes |
| `voice_language` | body | `string` | yes |
| `variables[]` | body | `array<object>` | yes |
| `video_name` | body | `string` | no |
| `avatar_id` | body | `number` | no |
| `avatar_type` | body | `number` | no |
| `voice_id` | body | `string` | no |
| `captions_enabled` | body | `boolean` | no |
| `background_music_id` | body | `number` | no |
| `disable_random_trans` | body | `boolean` | no |
| `disable_random_moving` | body | `boolean` | no |
| `disable_trans` | body | `boolean` | no |
| `disable_moving` | body | `boolean` | no |
