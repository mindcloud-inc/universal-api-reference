# Sequenzy: Trigger Event

Triggers an event for a subscriber in Sequenzy.

```
POST https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/trigger-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/trigger-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/trigger-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Subscriber email address. |
| `event` | string | yes | Event name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {
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
| `event.definitionCreated` | boolean |  |
| `event.id` | string |  |
| `event.name` | string |  |
| `subscriber.created` | boolean |  |
| `subscriber.email` | string |  |
| `subscriber.id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `POST /subscribers/events` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-event.md) for the provider-specific parameters and requirements.

