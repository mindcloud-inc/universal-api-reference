# Fliz: Create video

Creates a new video in Fliz.

```
POST https://connect.mindcloud.co/v1/universal/fliz/latest/actions/create-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/create-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "format": "0",
  "lang": "en"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fliz/latest/actions/create-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string",
    "format": "0",
    "lang": "en"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the product, article, or ad. |
| `description` | string | yes | The description of the video content to generate. |
| `format` | string | yes | The output video format. One of: `0`, `1`, `2`. |
| `lang` | string | yes | Two-character ISO 639-1 language code for the video. Default: `en`. |
| `category` | string | no | Type of video to generate: ad, product, or article. One of: `0`, `1`, `2`. Default: `article`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image_style` | string | no | Visual style applied to generated images. Default: `hyperrealistic`. |
| `script_style` | string | no | Narrative style for the generated script. Default: `news_social_media_style`. |
| `is_automatic` | boolean | no | Whether the video will be generated to the end automatically. Default: `false`. |
| `music_volume` | number | no | Music volume from 0 to 100. Default: `15`. |
| `caption_style` | string | no | Caption style preset. One of: `0`, `1`, `2`, `3`. |
| `caption_position` | string | no | Caption vertical position on screen. One of: `0`, `1`. |
| `caption_font` | string | no | Font family for captions. One of: `0`, `1`, `2`, `3`, `4`. |
| `caption_color` | string | no | Caption text color in hexadecimal format. Example: `#FFFFFF`. |
| `caption_uppercase` | boolean | no | If true, caption text is displayed in uppercase. |
| `voice_id` | string | no | Custom voice ID from the voices endpoint. |
| `music_id` | string | no | Music file ID from the musics endpoint. |
| `music_url` | string | no | Custom music URL to use as background audio. |
| `webhook_url` | string | no | Webhook URL called when rendering completes or errors. |
| `site_url` | string | no | URL displayed in the call to action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number | Credits consumed by the video creation. |
| `videoId` | string | Created video UUID. |

## Native endpoint

Through the native Fliz API, this operation is `POST /api/rest/video` (base URL `https://app.fliz.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video.md) for the provider-specific parameters and requirements.

