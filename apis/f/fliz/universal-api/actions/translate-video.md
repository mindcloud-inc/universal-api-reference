# Fliz: Translate video

Creates a translated video in Fliz.

```
POST https://connect.mindcloud.co/v1/universal/fliz/latest/actions/translate-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/translate-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from_video_id": "string",
  "new_lang": "fr"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fliz/latest/actions/translate-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from_video_id": "string",
    "new_lang": "fr"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from_video_id` | string | yes | The UUID of the existing video to translate. |
| `new_lang` | string | yes | Target two-character ISO 639-1 language code. Default: `fr`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `is_automatic` | boolean | no | Whether the translated video will be generated to the end automatically. Default: `false`. |
| `webhook_url` | string | no | Webhook URL called when rendering completes or errors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "newVideoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number | Credits consumed by the translation. |
| `newVideoId` | string | Translated video UUID. |

## Native endpoint

Through the native Fliz API, this operation is `POST /api/rest/videos/:from_video_id/translate` (base URL `https://app.fliz.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-video.md) for the provider-specific parameters and requirements.

