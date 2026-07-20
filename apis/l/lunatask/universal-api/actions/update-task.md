# Lunatask: Update Task



```
PUT https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunatask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/update-task', {
  method: 'PUT',
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
| `id` | string | yes | The ID of the task to update |
| `name` | string | no | The new name of the task |
| `note` | string | no | The new note of the task in Markdown |
| `status` | string | no | The new status of the task |
| `motivation` | string | no | The new motivation value of the task |
| `scheduledOn` | date | no | ISO-8601 formatted date the task is scheduled on |

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

Through the native Lunatask API, this operation is `PUT /tasks/:id` (base URL `https://api.lunatask.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

