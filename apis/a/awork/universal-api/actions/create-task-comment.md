# Awork: Create Task Comment

Creates a task comment in Awork.

```
POST https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "message": "Hey team, the customer loved the latest designs!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "message": "Hey team, the customer loved the latest designs!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The id of the task. |
| `message` | string | yes | The message of the comment. Example: `Hey team, the customer loved the latest designs!`. |
| `previews` | string | no | The preview URLs to show a preview for. Accepts multiple values as an array. Example: `https://www.awork.com/en/blog/automatic-project-management/`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inReplyToCommentId` | string | no | The parent comment this comment replies to. |
| `userId` | string | no | The id of the user who created the comment. If omitted, Awork defaults to the current user. |
| `isHiddenForConnectUsers` | boolean | no | Whether the comment is hidden for connect users. If omitted, Awork keeps the default visible behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "entity": {
        "id": "string",
        "name": "Ava Chen"
      },
      "entityId": "string",
      "entityType": "string",
      "formattedMessage": "string",
      "id": "string",
      "isHiddenForConnectUsers": true,
      "mentions": {
        "everyUserHadPermissions": true
      },
      "message": "string",
      "plainFormattedMessage": "string",
      "project": {
        "id": "string",
        "name": "Ava Chen"
      },
      "resourceVersion": 1,
      "task": {
        "id": "string",
        "name": "Ava Chen"
      },
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "user": {
        "firstName": "Ava",
        "hasImage": true,
        "id": "string",
        "isExternal": true,
        "lastName": "Chen"
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdOn` | date |  |
| `entity.id` | string |  |
| `entity.name` | string |  |
| `entityId` | string |  |
| `entityType` | string |  |
| `formattedMessage` | string |  |
| `id` | string |  |
| `isHiddenForConnectUsers` | boolean |  |
| `mentions.everyUserHadPermissions` | boolean |  |
| `message` | string |  |
| `plainFormattedMessage` | string |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `resourceVersion` | number |  |
| `task.id` | string |  |
| `task.name` | string |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |
| `user.firstName` | string |  |
| `user.hasImage` | boolean |  |
| `user.id` | string |  |
| `user.isExternal` | boolean |  |
| `user.lastName` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Awork API, this operation is `POST /tasks/:taskId/comments` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-comment.md) for the provider-specific parameters and requirements.

