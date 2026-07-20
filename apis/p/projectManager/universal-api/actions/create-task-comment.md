# ProjectManager: Create Task Comment

Creates a new task comment in ProjectManager.

```
POST https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "22222222-2222-2222-2222-222222222222"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "22222222-2222-2222-2222-222222222222"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The unique ID number of the task being commented upon Example: `22222222-2222-2222-2222-222222222222`. |
| `text` | string | no | The text of the comment to add to the discussion, in Markdown format. Discussion comments are formatted using [Markdown](https://www.markdownguide.org/) and users should be aware that HTML embedding is not permitted due to the risk of cross-site attacks and other embedding challenges. Example: `MindCloud sample text.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discussionCommentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discussionCommentId` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `POST /api/data/tasks/:taskId/comments` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-comment.md) for the provider-specific parameters and requirements.

