# ProjectManager: Delete Task

Deletes an existing task from ProjectManager.

```
DELETE https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/delete-task?connectionId=$CONNECTION_ID&taskId=22222222-2222-2222-2222-222222222222" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "22222222-2222-2222-2222-222222222222"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/delete-task?${params}`, {
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
| `taskId` | string | yes | Unique identifier of the Task to delete Example: `22222222-2222-2222-2222-222222222222`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changeSetId": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changeSetId` | string |  |
| `id` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `DELETE /api/data/tasks/:taskId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

