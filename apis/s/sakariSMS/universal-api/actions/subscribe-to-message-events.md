# Sakari SMS: Subscribe To Message Events

Subscribes to message events in Sakari SMS.

```
POST https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/subscribe-to-message-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/subscribe-to-message-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/subscribe-to-message-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes |  |
| `eventTypes[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destination": "string",
      "eventTypes": [
        "string"
      ],
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destination` | string |  |
| `eventTypes` | array<string> |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `POST /v1/accounts/:accountId/webhooks` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-message-events.md) for the provider-specific parameters and requirements.

