# OnceHub: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Customer booking updates",
  "url": "https://example.com/oncehub/webhooks",
  "events": "booking"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Customer booking updates",
    "url": "https://example.com/oncehub/webhooks",
    "events": "booking"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Unique name for the webhook subscription. Example: `Customer booking updates`. |
| `url` | string | yes | Full HTTPS endpoint OnceHub should call when subscribed events occur. Example: `https://example.com/oncehub/webhooks`. |
| `events` | list<string> | yes | Event types that should trigger the webhook subscription. One of: `booking`, `booking.canceled`, `booking.canceled_reschedule_requested`, `booking.canceled_then_rescheduled`, `booking.completed`, `booking.no_show`, `booking.rescheduled`, `booking.scheduled`, `conversation`, `conversation.abandoned`, `conversation.closed`, `conversation.started`. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationTime": "2026-05-07T12:00:00.000Z",
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationTime` | date |  |
| `events[]` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `url` | string |  |

## Native endpoint

Through the native OnceHub API, this operation is `POST /v1/webhooks` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

