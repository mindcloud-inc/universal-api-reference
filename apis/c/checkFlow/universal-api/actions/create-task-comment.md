# CheckFlow: Create Task Comment



```
POST https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "5678",
  "commentHtml": "<p>MindCloud smoke test comment</p>",
  "createdByUserId": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "5678",
    "commentHtml": "<p>MindCloud smoke test comment</p>",
    "createdByUserId": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | The ID of the task to comment on. Example: `5678`. |
| `commentHtml` | string | yes | The comment content as an HTML string. Example: `<p>MindCloud smoke test comment</p>`. |
| `createdByUserId` | number | yes | The ID of the user creating the comment. Use 0 for anonymous. Example: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CheckFlow API returns.

## Native endpoint

Through the native CheckFlow API, this operation is `POST /api/task/comment` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-comment.md) for the provider-specific parameters and requirements.

