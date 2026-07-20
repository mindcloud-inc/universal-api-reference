# Dart: Create Task Comment

Creates a task comment in Dart.

```
POST https://connect.mindcloud.co/v1/universal/dart/latest/actions/create-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dart/latest/actions/create-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dart/latest/actions/create-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item.parentId` | string | no |  |
| `item.taskId` | string | no |  |
| `item.text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "htmlUrl": "https://example.com",
      "id": "string",
      "taskId": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `htmlUrl` | string |  |
| `id` | string |  |
| `taskId` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Dart API, this operation is `POST /comments` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-comment.md) for the provider-specific parameters and requirements.

