# Conversion Tools: Delete Task Files Immediately

Permanently deletes a task's files from Conversion Tools.

```
DELETE https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/delete-task-files-immediately
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conversion Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/delete-task-files-immediately?connectionId=$CONNECTION_ID&taskId=28f2f333593949fe9b33c859c6d339de" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "28f2f333593949fe9b33c859c6d339de"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/delete-task-files-immediately?${params}`, {
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
| `taskId` | string | yes | The task ID whose files should be deleted. Example: `28f2f333593949fe9b33c859c6d339de`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Conversion Tools API returns.

## Native endpoint

Through the native Conversion Tools API, this operation is `POST /tasks/:taskId/delete` (base URL `https://api.conversiontools.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task-files-immediately.md) for the provider-specific parameters and requirements.

