# Manus: Update Task

Updates task metadata in Manus.

```
PUT https://connect.mindcloud.co/v1/universal/manus/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Manus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manus/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manus/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The ID of the task to update |
| `title` | string | no | New title for the task |
| `enableShared` | boolean | no | Make the task publicly accessible |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enableVisibleInTaskList` | boolean | no | Show the task in the Manus web app task list |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string",
      "taskTitle": "string",
      "taskUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string |  |
| `taskTitle` | string |  |
| `taskUrl` | string |  |

## Native endpoint

Through the native Manus API, this operation is `PUT /tasks/:task_id` (base URL `https://api.manus.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

