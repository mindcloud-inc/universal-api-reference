# Teamgate: Create Task

Creates a new task in Teamgate.

```
POST https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Follow up with prospect"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Follow up with prospect"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Task name. Example: `Follow up with prospect`. |

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

Through the native Teamgate API, this operation is `POST /events` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

