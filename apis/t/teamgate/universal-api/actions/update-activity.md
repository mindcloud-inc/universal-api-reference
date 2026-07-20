# Teamgate: Update Activity

Updates an activity in Teamgate.

```
PUT https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | Unique key of the activity. |
| `name` | string | no | Updated activity name. Example: `Codex Stage 3 Task Updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDay": "string",
      "canEdit": "string",
      "canView": "string",
      "companies": [
        {}
      ],
      "completed": {},
      "created": {},
      "deals": [
        {}
      ],
      "end": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDeleted": "string",
      "isSecret": "string",
      "name": "Ava Chen",
      "owner": {},
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string",
      "updated": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | string |  |
| `canEdit` | string |  |
| `canView` | string |  |
| `companies` | array<object> |  |
| `completed` | object |  |
| `created` | object |  |
| `deals` | array<object> |  |
| `end` | date |  |
| `id` | number |  |
| `isDeleted` | string |  |
| `isSecret` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `start` | date |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | object |  |
| `value` | string |  |

## Native endpoint

Through the native Teamgate API, this operation is `PUT /events/{{eventId}}` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity.md) for the provider-specific parameters and requirements.

