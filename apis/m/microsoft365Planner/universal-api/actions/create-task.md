# Microsoft 365 Planner: Create Task



```
POST https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Update client list",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Update client list",
    "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title for the new Planner task. Example: `Update client list`. |
| `planId` | string | yes | Planner plan ID where the task should be created. Example: `xqQg5FS2LkCp935s-FIFm2QAFkHM`. |
| `bucketId` | string | no | Planner bucket ID for the new task. Example: `hsOf2dhOJkqyYYZEtdzDe2QAIUCR`. |
| `dueDateTime` | string | no | Optional task due date/time in ISO 8601 format. Example: `2026-04-30T17:00:00Z`. |
| `startDateTime` | string | no | Optional task start date/time in ISO 8601 format. Example: `2026-04-14T09:00:00Z`. |
| `percentComplete` | number | no | Optional completion percentage from 0 to 100. Example: `0`. |
| `priority` | number | no | Optional Planner priority value from 0 to 10. Example: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucketId": "string",
      "dueDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "percentComplete": 1,
      "planId": "string",
      "priority": 1,
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketId` | string |  |
| `dueDateTime` | date |  |
| `id` | string |  |
| `percentComplete` | number |  |
| `planId` | string |  |
| `priority` | number |  |
| `startDateTime` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `POST /v1.0/planner/tasks` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

