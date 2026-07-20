# Freedcamp: Update Task

Updates an existing task in Freedcamp.

```
PUT https://connect.mindcloud.co/v1/universal/freedcamp/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freedcamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freedcamp/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freedcamp/latest/actions/update-task', {
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
| `taskId` | string | yes | The Freedcamp task ID. |
| `title` | string | no | Updated task title. |
| `description` | string | no | Updated task description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "projectId": "string",
      "statusTitle": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `projectId` | string |  |
| `statusTitle` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Freedcamp API, this operation is `POST /api/v1/tasks/:taskId` (base URL `https://freedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

