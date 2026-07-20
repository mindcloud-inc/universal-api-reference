# Vadootv: Generate video

Creates an AI video in Vadootv.

```
POST https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topic` | list<string> | no | Topic of the video. Use Custom to provide a manual prompt. One of: `Bedtime Stories`, `Custom`, `Dangerous Sea Videos`, `ELI5`, `Emotional Pet Stories`, `Fun Facts`, `Interesting History`, `Life Pro Tips`, `Long Form Jokes`, `Motivational`, `POV History`, `Pet Animal Comedy`, `Philosophy`, `Random AI Story`, `Scary Stories`, `Travel Content`, `True Crime Stories`. Default: `Random AI Story`. |
| `duration` | list<string> | no | Target duration code. One of: `10 min`, `120-180`, `30-60`, `5 min`, `60-90`, `90-120`. Default: `30-60`. |
| `voice` | string | no | AI voice name. Default: `Onyx`. Example: `Onyx`. |
| `language` | string | no | Video language. Default: `English`. Example: `English`. |
| `aspect_ratio` | list<string> | no | Output video aspect ratio. One of: `16:9`, `1:1`, `9:16`. Default: `9:16`. |
| `style` | string | no | Visual style theme. Default: `None`. Example: `None`. |
| `theme` | string | no | Subtitle theme name. Default: `Hormozi_1`. Example: `Hormozi_1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | no | Story details to generate. Required when topic is Custom. Example: `Story details when topic is Custom`. |
| `bg_music` | string | no | Background music name. Example: `Another-love`. |
| `bg_music_volume` | number | no | Background music volume from 0 to 100. Default: `100`. Example: `100`. |
| `speed` | number | no | Voiceover playback speed from 0.5 to 2.0. Default: `1`. Example: `1.0`. |
| `use_ai` | number | no | Set to 0 to provide a complete script manually in the prompt. Default: `1`. Example: `1`. |
| `include_voiceover` | number | no | Set to 0 to disable voiceover. Default: `1`. Example: `1`. |
| `custom_instructions` | string | no | Additional creative instructions for the AI. Example: `Extra creative guidance`. |
| `url` | string | no | Blog or article URL to convert into a video. Example: `https://example.com/article`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "vid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `vid` | string | Video ID for the generated AI video. |

## Native endpoint

Through the native Vadootv API, this operation is `POST /api/generate_video` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-video.md) for the provider-specific parameters and requirements.

