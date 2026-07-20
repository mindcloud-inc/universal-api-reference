# KanbanFlow: Delete manual time entry

Deletes an existing manual time entry from KanbanFlow.

```
DELETE https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/delete-manual-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/delete-manual-time-entry?connectionId=$CONNECTION_ID&taskId=string&manualTimeEntryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string",
  "manualTimeEntryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/delete-manual-time-entry?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The KanbanFlow task ID. |
| `manualTimeEntryId` | string | yes | The KanbanFlow manual time entry ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KanbanFlow API returns.

## Native endpoint

Through the native KanbanFlow API, this operation is `DELETE /tasks/:taskId/manual-time-entries/:manualTimeEntryId` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-manual-time-entry.md) for the provider-specific parameters and requirements.

