# WebinarGeek: Subscribe to Broadcast



```
POST https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/subscribe-to-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebinarGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/subscribe-to-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcastId": 1,
  "firstname": "Ava",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/subscribe-to-broadcast', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcastId": 1,
    "firstname": "Ava",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcastId` | number | yes | ID of the broadcast to subscribe the viewer to |
| `firstname` | string | yes | First name of the subscribing user |
| `email` | string | yes | Email address of the subscribing user |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmationLink": "https://example.com",
      "createdAt": 1,
      "eligibleToWatch": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "firstname": "Ava",
      "id": 1,
      "unsubscribed": true,
      "watchLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmationLink` | string |  |
| `createdAt` | number |  |
| `eligibleToWatch` | boolean |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `firstname` | string |  |
| `id` | number |  |
| `unsubscribed` | boolean |  |
| `watchLink` | string |  |

## Native endpoint

Through the native WebinarGeek API, this operation is `POST /broadcasts/:broadcastId/subscriptions` (base URL `https://app.webinargeek.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-broadcast.md) for the provider-specific parameters and requirements.

