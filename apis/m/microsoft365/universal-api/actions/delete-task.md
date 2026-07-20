# Microsoft 365: Delete Task

Deletes a task from Microsoft 365.

```
DELETE https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/delete-task?connectionId=$CONNECTION_ID&taskListId=AQMkAD...&taskId=AQMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskListId": "AQMkAD...",
  "taskId": "AQMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/delete-task?${params}`, {
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
| `taskListId` | string | yes | Example: `AQMkAD...`. |
| `taskId` | string | yes | Example: `AQMkAG...`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 API returns.

## Native endpoint

Through the native Microsoft 365 API, this operation is `DELETE /v1.0/me/todo/lists/{{taskListId}}/tasks/{{taskId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

