# KanbanFlow: Update manual time entry

Updates an existing manual time entry in KanbanFlow.

```
PUT https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/update-manual-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/update-manual-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "manualTimeEntryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/update-manual-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "manualTimeEntryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The KanbanFlow task ID. |
| `manualTimeEntryId` | string | yes | The KanbanFlow manual time entry ID. |
| `startTimestamp` | string | no | The UTC timestamp when the entry started. |
| `endTimestamp` | string | no | The UTC timestamp when the entry ended. |
| `comment` | string | no | A short comment for the time entry. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KanbanFlow API returns.

## Native endpoint

Through the native KanbanFlow API, this operation is `POST /tasks/:taskId/manual-time-entries/:manualTimeEntryId` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-manual-time-entry.md) for the provider-specific parameters and requirements.

