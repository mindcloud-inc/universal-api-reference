# EventGeek: Create Event

Creates a new event in EventGeek.

```
POST https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud delete event disposable 2026-04-21 16:20",
  "status": "COMMITTED",
  "team_id": "VGVhbS0xMDcwMQ"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud delete event disposable 2026-04-21 16:20",
    "status": "COMMITTED",
    "team_id": "VGVhbS0xMDcwMQ"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Event name. Default: `MindCloud delete event disposable 2026-04-21 16:20`. |
| `status` | string | yes | Event status. Default: `COMMITTED`. |
| `team_id` | string | yes | Team that owns the event. Default: `VGVhbS0xMDcwMQ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_fields": {},
      "end_date": "string",
      "id": "string",
      "location": "string",
      "name": "Ava Chen",
      "start_date": "string",
      "status": "string",
      "team_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_fields` | object |  |
| `end_date` | string |  |
| `id` | string |  |
| `location` | string |  |
| `name` | string |  |
| `start_date` | string |  |
| `status` | string |  |
| `team_id` | string |  |

## Native endpoint

Through the native EventGeek API, this operation is `POST /events` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

