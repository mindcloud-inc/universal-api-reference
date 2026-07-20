# Create Template to Video Task with DomoAI

Creates a new template-to-video task in DomoAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/video/template2video`
- **Base URL:** `https://api.domoai.com`
- **Official documentation:** [Create Template to Video Task](https://docs.domoai.app/api-reference/ai-video/template-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | body | `list` | yes | The DomoAI template preset to use. Accepted values: `360_view`, `crane_up`, `french_kiss`, `groove_dance`, `hug`, `kiss`, `kissing_screen`, `looping_animation`, `zoom_in`, `zoom_out`. |
| `images[].domoai_uri` | body | `string` | yes | A domoai_uri from the Upload File action. |
| `images[].bytes_base64_encoded` | body | `string` | no | Base64-encoded image bytes for the template input image. |
| `seconds` | body | `number` | yes | Output video duration in seconds. |
| `prompt` | body | `string` | no | Optional prompt to guide the template animation. |
| `aspect_ratio` | body | `list` | no | Output video aspect ratio. Accepted values: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |
| `callback_url` | body | `string` | no | Optional URL that DomoAI should notify when task status changes. |
