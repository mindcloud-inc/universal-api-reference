# Morningmate: Create Task

Creates a task in a Morningmate project.

```
POST https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "registerId": "string",
  "title": "string",
  "contents": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "registerId": "string",
    "title": "string",
    "contents": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `registerId` | string | yes |  |
| `title` | string | yes |  |
| `contents` | string | yes |  |
| `status` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "postId": "string",
      "projectId": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `postId` | string | Created post identifier backing the task. |
| `projectId` | string | Morningmate project identifier. |
| `taskId` | string | Created task identifier. |

## Native endpoint

Through the native Morningmate API, this operation is `POST /v1/posts/projects/[:projectId]/tasks` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

