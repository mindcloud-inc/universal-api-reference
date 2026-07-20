# ProjectManager: Retrieve Task Comments

Retrieves task comments from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task-comments?connectionId=$CONNECTION_ID&taskId=22222222-2222-2222-2222-222222222222" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "22222222-2222-2222-2222-222222222222"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-task-comments?${params}`, {
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
| `taskId` | string | yes | The unique ID number of the task to retrieve comments Example: `22222222-2222-2222-2222-222222222222`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "authorName": "Ava Chen",
      "createDate": "string",
      "discussionCommentId": "string",
      "emoji": {
        "name": "Ava Chen",
        "userIds": [
          "string"
        ]
      },
      "files": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "id": "string",
      "modifyDate": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `authorName` | string |  |
| `createDate` | string |  |
| `discussionCommentId` | string |  |
| `emoji.name` | string |  |
| `emoji.userIds` | array<string> |  |
| `files.id` | string |  |
| `files.name` | string |  |
| `files.url` | string |  |
| `id` | string |  |
| `modifyDate` | string |  |
| `text` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/tasks/:taskId/comments` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task-comments.md) for the provider-specific parameters and requirements.

