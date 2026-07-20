# Sequenzy: Trigger Events (Bulk)

Triggers events for multiple subscribers in Sequenzy.

```
POST https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/trigger-events-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/trigger-events-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "events": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/trigger-events-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "events": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Subscriber email address. |
| `events` | list<object> | yes | Events to trigger in bulk. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": {
        "definitionCreated": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "subscriber": {
        "created": true,
        "email": "ava@example.com",
        "id": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> |  |
| `events.definitionCreated` | boolean |  |
| `events.id` | string |  |
| `events.name` | string |  |
| `subscriber.created` | boolean |  |
| `subscriber.email` | string |  |
| `subscriber.id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `POST /subscribers/events/bulk` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-events-bulk.md) for the provider-specific parameters and requirements.

