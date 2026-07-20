# Create Reel (V1) with Reka Vision

Creates highlight reels in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/clips`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Create Reel (V1)](https://docs.reka.ai/vision/api-reference/v-1/create-reel-v-1-clips-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reel_quality` | query | `list<string>` | no | Accepted values: `fallback`, `full_video`, `lite`, `premium`. |
| `video_urls[]` | body | `array<string>` | yes | — |
| `prompt` | body | `string` | no | — |
| `generation_config` | body | `object` | no | — |
| `generation_config.template` | body | `list<string>` | no | Accepted values: `caption_only`, `compilation`, `moments`, `trailer`, `voiceover`. |
| `generation_config.num_generations` | body | `number` | no | — |
| `generation_config.min_duration_seconds` | body | `number` | no | — |
| `generation_config.max_duration_seconds` | body | `number` | no | — |
| `generation_config.source_start_time` | body | `number` | no | — |
| `generation_config.source_end_time` | body | `number` | no | — |
| `rendering_config` | body | `object` | no | — |
| `rendering_config.show_watermark` | body | `boolean` | no | — |
| `rendering_config.subtitles` | body | `boolean` | no | — |
| `rendering_config.aspect_ratio` | body | `list<string>` | no | Accepted values: `16:9`, `1:1`, `4:5`, `9:16`, `9:16-split`. |
| `rendering_config.resolution` | body | `list<string>` | no | Accepted values: `1080`, `240`, `360`, `480`, `720`. |
| `rendering_config.caption_style` | body | `object` | no | — |
| `rendering_config.caption_style.desired_font_size` | body | `number` | no | — |
| `rendering_config.caption_style.text_transform` | body | `list<string>` | no | Accepted values: `initial`, `lowercase`, `uppercase`. |
| `rendering_config.caption_style.text_color` | body | `string` | no | — |
| `rendering_config.caption_style.highlight_color` | body | `string` | no | — |
| `rendering_config.caption_style.stroke_color` | body | `string` | no | — |
| `rendering_config.caption_style.position` | body | `list<string>` | no | Accepted values: `bottom`, `middle`, `top`. |
| `rendering_config.caption_style.font_family` | body | `list<string>` | no | Accepted values: `Bangers`, `BebasNeue`, `CaptionFont`, `Lato`, `RobotoCondensed`. |
| `stream` | body | `boolean` | no | — |
