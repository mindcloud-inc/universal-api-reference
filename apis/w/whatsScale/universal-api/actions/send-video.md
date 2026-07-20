# WhatsScale: Send Video

Creates a video send job in WhatsScale.

```
POST https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "file": "string",
  "session": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
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
| `caption` | string | no | Optional video caption. |
| `chatId` | string | yes | Recipient chat ID. |
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

Through the native WhatsScale API, this operation is `POST /api/sendVideo` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-video.md) for the provider-specific parameters and requirements.

