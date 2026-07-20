# ProProfs Project: Create Comment

Creates a new comment in ProProfs Project.

```
POST https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "comment": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "comment": "string",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | yes | The comment text. |
| `projectId` | string | yes | The project ID that will own the comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "commentId": "string",
      "dateCreated": "string",
      "dateModified": "string",
      "filename": "Ava Chen",
      "filepath": "string",
      "note": "string",
      "parentId": "string",
      "projectId": "string",
      "subtaskId": "string",
      "taskId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `commentId` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `filename` | string |  |
| `filepath` | string |  |
| `note` | string |  |
| `parentId` | string |  |
| `projectId` | string |  |
| `subtaskId` | string |  |
| `taskId` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `POST /comments/{{project_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

