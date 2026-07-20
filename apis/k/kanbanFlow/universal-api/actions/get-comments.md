# KanbanFlow: Get comments

Retrieves all comments for a KanbanFlow task.

```
GET https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-comments?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-comments?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorUserId": "string",
      "createdTimestamp": "string",
      "text": "string",
      "updatedTimestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorUserId` | string |  |
| `createdTimestamp` | string |  |
| `text` | string |  |
| `updatedTimestamp` | string |  |

## Native endpoint

Through the native KanbanFlow API, this operation is `GET /tasks/:taskId/comments` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comments.md) for the provider-specific parameters and requirements.

