# WhatsScale: Post Video Story

Creates a video story job in WhatsScale.

```
POST https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/post-video-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/post-video-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "session": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/post-video-story', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "session": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caption` | string | no | Optional video story caption. |
| `file` | string | yes | Public URL to the video. |
| `session` | string | yes | Session name from /api/sessions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native WhatsScale API, this operation is `POST /api/status/video` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-video-story.md) for the provider-specific parameters and requirements.

