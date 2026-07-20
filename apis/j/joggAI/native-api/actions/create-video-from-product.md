# Create Video From Product with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/create_video_from_product`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Create Video From Product](https://docs.jogg.ai/api-reference/v2/Video/CreateVideoFromProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio.music_id` | body | `number` | no | Optional background music ID. |
| `avatar.id` | body | `number` | yes | Avatar ID to use in the product video. |
| `avatar.type` | body | `number` | yes | 0 for public avatars, 1 for custom avatars. |
| `override_script` | body | `string` | no | Custom script to use instead of AI-generated copy. |
| `product_id` | body | `string` | yes | Product ID returned by Create Product. |
| `script.language` | body | `string` | yes | Script language such as english. |
| `script.style` | body | `string` | yes | Script style such as Storytime or Discovery. |
| `video_spec.aspect_ratio` | body | `string` | yes | Video aspect ratio: portrait, landscape, or square. |
| `video_spec.caption` | body | `boolean` | no | Whether captions should be included. |
| `video_spec.length` | body | `string` | yes | Video length in seconds: 15, 30, or 60. |
| `visual_style` | body | `string` | no | Visual style name from List Visual Styles. |
| `voice.id` | body | `string` | yes | Voice ID for the generated narration. |
