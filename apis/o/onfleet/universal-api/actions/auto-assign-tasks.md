# Onfleet: Auto-Assign Tasks

Assigns tasks to workers automatically in Onfleet.

```
PUT https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/auto-assign-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/auto-assign-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasks[]": [
    "string"
  ],
  "options.mode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/auto-assign-tasks', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tasks[]": ["string"],
    "options.mode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tasks[]` | array<string> | yes | An array of task IDs to assign. |
| `options.mode` | string | yes | The desired automatic assignment mode. Either distance or load. |
| `options.teams[]` | array<string> | no | An array of team IDs to consider for automatic assignment. |
| `options.maxAssignedTaskCount` | number | no | The maximum number of tasks a worker can have after automatic assignment. |
| `options.considerDependencies` | boolean | no | Whether to include dependency families in the assignment operation. |
| `options.excludedWorkerIds[]` | array<string> | no | One or more worker IDs that should not be considered in assignment calculations. |
| `options.restrictAutoAssignmentToTeam` | boolean | no | Whether to restrict auto-assignment strictly to the provided teams. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTasks": {},
      "assignedTasksCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTasks` | object |  |
| `assignedTasksCount` | number |  |

## Native endpoint

Through the native Onfleet API, this operation is `POST /tasks/autoAssign` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auto-assign-tasks.md) for the provider-specific parameters and requirements.

