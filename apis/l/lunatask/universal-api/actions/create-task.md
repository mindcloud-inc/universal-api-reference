# Lunatask: Create Task



```
POST https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunatask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "areaId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "areaId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `areaId` | string | yes | The Area ID of the list where the task should be created |
| `goalId` | string | no | The ID of the goal where the task should be created |
| `name` | string | no | The name of the task |
| `note` | string | no | The note attached to the task in Markdown |
| `status` | string | no | The status of the task |
| `motivation` | string | no | The motivation value of the task |
| `eisenhower` | number | no | The quadrant on the Eisenhower matrix |
| `estimate` | number | no | The estimate of the task in minutes |
| `priority` | number | no | Priority of the task |
| `scheduledOn` | date | no | ISO-8601 formatted date the task is scheduled on |
| `completedAt` | date | no | ISO-8601 formatted time when the task was completed |
| `source` | string | no | Identification of the external system where the task is coming from |
| `sourceId` | string | no | The ID of the record in the external system |

## Response

```json
{
  "success": true,
  "data": [
    {
      "areaId": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "eisenhower": 1,
      "estimate": 1,
      "goalId": "string",
      "id": "string",
      "motivation": "string",
      "previousStatus": "string",
      "priority": 1,
      "progress": 1,
      "scheduledOn": "2026-05-07T12:00:00.000Z",
      "sources": [
        "string"
      ],
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areaId` | string |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `eisenhower` | number |  |
| `estimate` | number |  |
| `goalId` | string |  |
| `id` | string |  |
| `motivation` | string |  |
| `previousStatus` | string |  |
| `priority` | number |  |
| `progress` | number |  |
| `scheduledOn` | date |  |
| `sources` | array |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunatask API, this operation is `POST /tasks` (base URL `https://api.lunatask.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

