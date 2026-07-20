# WhatsScale: Post Text Story

Creates a text story job in WhatsScale.

```
POST https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/post-text-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/post-text-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "session": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/post-text-story', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "session": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `backgroundColor` | string | no | Optional hex background color for the text story. |
| `font` | number | no | Optional WhatsApp story font style number. |
| `session` | string | yes | Session name from /api/sessions. |
| `text` | string | yes | Status text. |

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

Through the native WhatsScale API, this operation is `POST /api/status/text` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-text-story.md) for the provider-specific parameters and requirements.

