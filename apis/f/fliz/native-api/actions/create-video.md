# Create video with Fliz

Creates a new video in Fliz.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/video`
- **Base URL:** `https://app.fliz.ai`
- **Official documentation:** [Create video](https://app.fliz.ai/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the product, article, or ad. |
| `description` | body | `string` | yes | The description of the video content to generate. |
| `format` | body | `string` | yes | The output video format. Accepted values: `0`, `1`, `2`. |
| `lang` | body | `string` | yes | Two-character ISO 639-1 language code for the video. |
| `category` | body | `string` | no | Type of video to generate: ad, product, or article. Accepted values: `0`, `1`, `2`. |
| `image_style` | body | `string` | no | Visual style applied to generated images. |
| `script_style` | body | `string` | no | Narrative style for the generated script. |
| `is_automatic` | body | `boolean` | no | Whether the video will be generated to the end automatically. |
| `music_volume` | body | `number` | no | Music volume from 0 to 100. |
| `caption_style` | body | `string` | no | Caption style preset. Accepted values: `0`, `1`, `2`, `3`. |
| `caption_position` | body | `string` | no | Caption vertical position on screen. Accepted values: `0`, `1`. |
| `caption_font` | body | `string` | no | Font family for captions. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `caption_color` | body | `string` | no | Caption text color in hexadecimal format. |
| `caption_uppercase` | body | `boolean` | no | If true, caption text is displayed in uppercase. |
| `voice_id` | body | `string` | no | Custom voice ID from the voices endpoint. |
| `music_id` | body | `string` | no | Music file ID from the musics endpoint. |
| `music_url` | body | `string` | no | Custom music URL to use as background audio. |
| `webhook_url` | body | `string` | no | Webhook URL called when rendering completes or errors. |
| `site_url` | body | `string` | no | URL displayed in the call to action. |
