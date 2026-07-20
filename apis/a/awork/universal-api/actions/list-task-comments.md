# Awork: List Task Comments

Retrieves task comments from Awork.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-task-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-task-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-task-comments?${params}`, {
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
| `taskId` | string | yes | The id of the task. |

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

Through the native Awork API, this operation is `GET /tasks/:taskId/comments` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-task-comments.md) for the provider-specific parameters and requirements.

