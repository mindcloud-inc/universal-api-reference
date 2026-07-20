# JoggAI: Create Video From Product



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-from-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-from-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "avatar.id": 1,
  "avatar.type": 1,
  "productId": "string",
  "script.language": "string",
  "script.style": "string",
  "video_spec.aspect_ratio": "string",
  "video_spec.length": "string",
  "voice.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-from-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "avatar.id": 1,
    "avatar.type": 1,
    "productId": "string",
    "script.language": "string",
    "script.style": "string",
    "video_spec.aspect_ratio": "string",
    "video_spec.length": "string",
    "voice.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audio.music_id` | number | no | Optional background music ID. |
| `avatar.id` | number | yes | Avatar ID to use in the product video. |
| `avatar.type` | number | yes | 0 for public avatars, 1 for custom avatars. |
| `overrideScript` | string | no | Custom script to use instead of AI-generated copy. |
| `productId` | string | yes | Product ID returned by Create Product. |
| `script.language` | string | yes | Script language such as english. |
| `script.style` | string | yes | Script style such as Storytime or Discovery. |
| `video_spec.aspect_ratio` | string | yes | Video aspect ratio: portrait, landscape, or square. |
| `video_spec.caption` | boolean | no | Whether captions should be included. |
| `video_spec.length` | string | yes | Video length in seconds: 15, 30, or 60. |
| `visualStyle` | string | no | Visual style name from List Visual Styles. |
| `voice.id` | string | yes | Voice ID for the generated narration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `videoId` | string |  |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/create_video_from_product` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-from-product.md) for the provider-specific parameters and requirements.

