# ProjectManager: Remove TaskTag from Task

Removes a task tag from a task in ProjectManager.

```
DELETE https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/remove-task-tag-from-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/remove-task-tag-from-task?connectionId=$CONNECTION_ID&taskId=22222222-2222-2222-2222-222222222222&value%5B%5D=sample&value%5B%5D=sample&value%5B%5D=sample&value%5B%5D=sample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "22222222-2222-2222-2222-222222222222",
  "value[]": "sample",
  "value[]": "sample",
  "value[]": "sample",
  "value[]": "sample"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/remove-task-tag-from-task?${params}`, {
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
| `taskId` | string | yes | The unique identifier of the Task for which we will remove existing TaskTags Example: `22222222-2222-2222-2222-222222222222`. |
| `value[]` | array | yes | Example: `sample`. |
| `value[]` | array | yes | Example: `sample`. |
| `value[]` | array | yes | Example: `sample`. |
| `value[]` | array | yes | Example: `sample`. |

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

Through the native ProjectManager API, this operation is `DELETE /api/data/tasks/:taskId/tags` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-task-tag-from-task.md) for the provider-specific parameters and requirements.

