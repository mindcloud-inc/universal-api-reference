# Create Text to Video Task with DomoAI

Creates a new text-to-video task in DomoAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/video/text2video`
- **Base URL:** `https://api.domoai.com`
- **Official documentation:** [Create Text to Video Task](https://docs.domoai.app/api-reference/ai-video/text-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | The text prompt that describes the video to generate. |
| `seconds` | body | `number` | yes | Output video duration in seconds. |
| `model` | body | `list` | no | The DomoAI text-to-video model version. Accepted values: `t2v-2.4-advanced`, `t2v-2.4-faster`. |
| `style` | body | `list` | no | Optional visual style preset. Accepted values: `90s_style`, `cartoon_game`, `flat_color_anime`, `japanese_anime`, `pixel`, `realistic`. |
| `aspect_ratio` | body | `list` | no | Output video aspect ratio. Accepted values: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |
| `callback_url` | body | `string` | no | Optional URL that DomoAI should notify when task status changes. |
