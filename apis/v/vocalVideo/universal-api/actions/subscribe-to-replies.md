# Vocal Video: Subscribe to Replies

Creates a reply webhook subscription in Vocal Video.

```
POST https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/subscribe-to-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vocal Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/subscribe-to-replies" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "zapUrl": "https://example.com/webhooks/vocal-video/replies"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/subscribe-to-replies', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "zapUrl": "https://example.com/webhooks/vocal-video/replies"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `zapUrl` | string | yes | Public webhook URL to notify when a new response is received. Example: `https://example.com/webhooks/vocal-video/replies`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Created callback subscription id. |

## Native endpoint

Through the native Vocal Video API, this operation is `POST /replies/subscribe` (base URL `https://vocalvideo.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-replies.md) for the provider-specific parameters and requirements.

