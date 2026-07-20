# Userflow: Track Event

Tracks a user or group event in Userflow.

```
POST https://connect.mindcloud.co/v1/universal/userflow/latest/actions/track-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/track-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userflow/latest/actions/track-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The event name to track. |
| `userId` | string | yes | The user associated with the event. |
| `attributes` | object | no | Optional event attributes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "phase": "string",
        "source": "string"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "group": {},
      "group_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "time": "2026-05-07T12:00:00.000Z",
      "user": {},
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Event attributes. |
| `attributes.phase` | string | Event phase. |
| `attributes.source` | string | Event source. |
| `created_at` | date | Event creation timestamp. |
| `group` | object | Associated group. |
| `group_id` | string | Associated group ID. |
| `id` | string | Event ID. |
| `name` | string | Event name. |
| `object` | string | Returned object type. |
| `time` | date | Event timestamp. |
| `user` | object | Associated user. |
| `user_id` | string | Associated user ID. |

## Native endpoint

Through the native Userflow API, this operation is `POST /events` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-event.md) for the provider-specific parameters and requirements.

