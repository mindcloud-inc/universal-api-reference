# Time Doctor: Create Task

Creates a new task in Time Doctor.

```
POST https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Task name. |
| `description` | string | no | Task description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "integration": {},
      "name": "Ava Chen",
      "project": {},
      "reporterId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `integration` | object |  |
| `name` | string |  |
| `project` | object |  |
| `reporterId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Time Doctor API, this operation is `POST /api/1.0/tasks` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

