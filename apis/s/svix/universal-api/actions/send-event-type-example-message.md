# Svix: Send Event Type Example Message

Sends an example event message to a Svix endpoint.

```
POST https://connect.mindcloud.co/v1/universal/svix/latest/actions/send-event-type-example-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/send-event-type-example-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/send-event-type-example-message', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        "string"
      ],
      "deliverAt": "string",
      "eventId": "string",
      "eventType": "string",
      "id": "string",
      "payload": {},
      "tags": [
        "string"
      ],
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<string> |  |
| `deliverAt` | string |  |
| `eventId` | string |  |
| `eventType` | string |  |
| `id` | string |  |
| `payload` | object |  |
| `tags` | array<string> |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Svix API, this operation is `POST /api/v1/app/{app_id}/endpoint/{endpoint_id}/send-example` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-event-type-example-message.md) for the provider-specific parameters and requirements.

