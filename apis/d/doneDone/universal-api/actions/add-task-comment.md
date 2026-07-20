# DoneDone: Add Task Comment

Creates a new task comment in DoneDone.

```
POST https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/add-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/add-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "taskId": 1,
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/add-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "projectId": 1,
    "taskId": 1,
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | DoneDone account ID. |
| `projectId` | number | yes | DoneDone internal project ID. |
| `taskId` | number | yes | DoneDone task ID. |
| `message` | string | yes | Comment body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider confirmation message. |

## Native endpoint

Through the native DoneDone API, this operation is `POST /:account_id/internal-projects/:internal_project_id/tasks/:task_id/comment-only` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-task-comment.md) for the provider-specific parameters and requirements.

