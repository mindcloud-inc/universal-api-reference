# Generate video with Vadootv

Creates an AI video in Vadootv.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate_video`
- **Base URL:** `https://aiapi.vadoo.tv`
- **Official documentation:** [Generate video](https://docs.vadoo.tv/docs/guide/ai-story/create-an-ai-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | body | `list<string>` | no | Topic of the video. Use Custom to provide a manual prompt. Accepted values: `Bedtime Stories`, `Custom`, `Dangerous Sea Videos`, `ELI5`, `Emotional Pet Stories`, `Fun Facts`, `Interesting History`, `Life Pro Tips`, `Long Form Jokes`, `Motivational`, `POV History`, `Pet Animal Comedy`, `Philosophy`, `Random AI Story`, `Scary Stories`, `Travel Content`, `True Crime Stories`. |
| `duration` | body | `list<string>` | no | Target duration code. Accepted values: `10 min`, `120-180`, `30-60`, `5 min`, `60-90`, `90-120`. |
| `prompt` | body | `string` | no | Story details to generate. Required when topic is Custom. |
| `voice` | body | `string` | no | AI voice name. |
| `language` | body | `string` | no | Video language. |
| `aspect_ratio` | body | `list<string>` | no | Output video aspect ratio. Accepted values: `16:9`, `1:1`, `9:16`. |
| `style` | body | `string` | no | Visual style theme. |
| `theme` | body | `string` | no | Subtitle theme name. |
| `bg_music` | body | `string` | no | Background music name. |
| `bg_music_volume` | body | `number` | no | Background music volume from 0 to 100. |
| `speed` | body | `number` | no | Voiceover playback speed from 0.5 to 2.0. |
| `use_ai` | body | `number` | no | Set to 0 to provide a complete script manually in the prompt. |
| `include_voiceover` | body | `number` | no | Set to 0 to disable voiceover. |
| `custom_instructions` | body | `string` | no | Additional creative instructions for the AI. |
| `url` | body | `string` | no | Blog or article URL to convert into a video. |
