# Livestorm: Create Event Session

Creates a new session for an event in Livestorm.

```
POST https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/create-event-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/create-event-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/create-event-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Event ID |
| `data.attributes.estimatedStartedAt` | date | no |  |
| `data.attributes.timezone` | string | no |  |
| `data.attributes.name` | string | no |  |
| `data.relationships.people[]` | array<object> | no |  |
| `data.relationships.people[].data.type` | string | no |  |
| `data.relationships.people[].data.id` | string | no |  |
| `data.relationships.people[].data.role` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "attendeesCount": 1,
        "canceledAt": 1,
        "createdAt": 1,
        "duration": 1,
        "endedAt": 1,
        "estimatedStartedAt": 1,
        "eventTypeId": "string",
        "name": "Ava Chen",
        "registrantsCount": 1,
        "roomLink": "https://example.com",
        "startedAt": 1,
        "status": "string",
        "timezone": "string",
        "updatedAt": 1
      },
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
| `attributes.attendeesCount` | number |  |
| `attributes.canceledAt` | number |  |
| `attributes.createdAt` | number |  |
| `attributes.duration` | number |  |
| `attributes.endedAt` | number |  |
| `attributes.estimatedStartedAt` | number |  |
| `attributes.eventTypeId` | string |  |
| `attributes.name` | string |  |
| `attributes.registrantsCount` | number |  |
| `attributes.roomLink` | string |  |
| `attributes.startedAt` | number |  |
| `attributes.status` | string |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `POST events/:id/sessions` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-session.md) for the provider-specific parameters and requirements.

