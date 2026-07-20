# ClickUp: Get Task



```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-task?${params}`, {
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
| `customTaskIds` | boolean | no |  |
| `teamId` | list | no |  |
| `includeMarkdownDescription` | boolean | no |  |
| `taskId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "creator": {
        "color": "string",
        "email": "ava@example.com",
        "id": 1,
        "profilePicture": {},
        "username": "Ava Chen"
      },
      "customId": "string",
      "customItemId": 1,
      "dateClosed": "string",
      "dateCreated": "string",
      "dateDone": "string",
      "dateUpdated": "string",
      "description": "string",
      "dueDate": "string",
      "folder": {
        "access": true,
        "hidden": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "list": {
        "access": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "orderindex": "string",
      "parent": "string",
      "permissionLevel": "string",
      "points": "string",
      "priority": "string",
      "project": {
        "access": true,
        "hidden": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "sharing": {
        "public": true,
        "publicFields": [
          "string"
        ],
        "publicShareExpiresOn": {},
        "seoOptimized": true,
        "token": {}
      },
      "space": {
        "id": "string"
      },
      "startDate": "string",
      "status": {
        "color": "string",
        "id": "string",
        "orderindex": 1,
        "status": "string",
        "type": "string"
      },
      "subtasks": [
        {
          "archived": true,
          "creator": {
            "color": "string",
            "email": "ava@example.com",
            "id": 1,
            "profilePicture": {},
            "username": "Ava Chen"
          },
          "customItemId": 1,
          "dateClosed": "string",
          "dateCreated": "string",
          "dateDone": "string",
          "dateUpdated": "string",
          "dueDate": "string",
          "id": "string",
          "name": "Ava Chen",
          "orderindex": "string",
          "parent": "string",
          "points": "string",
          "startDate": "string",
          "status": {
            "color": "string",
            "orderindex": 1,
            "status": "string",
            "type": "string"
          },
          "timeEstimate": "string",
          "timeSpent": 1,
          "topLevelParent": "string",
          "url": "https://example.com"
        }
      ],
      "teamId": "string",
      "textContent": "string",
      "timeEstimate": "string",
      "timeSpent": 1,
      "topLevelParent": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `creator.color` | string |  |
| `creator.email` | string |  |
| `creator.id` | number |  |
| `creator.profilePicture` | object |  |
| `creator.username` | string |  |
| `customId` | string |  |
| `customItemId` | number |  |
| `dateClosed` | string |  |
| `dateCreated` | string |  |
| `dateDone` | string |  |
| `dateUpdated` | string |  |
| `description` | string |  |
| `dueDate` | string |  |
| `folder.access` | boolean |  |
| `folder.hidden` | boolean |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `id` | string |  |
| `list.access` | boolean |  |
| `list.id` | string |  |
| `list.name` | string |  |
| `name` | string |  |
| `orderindex` | string |  |
| `parent` | string |  |
| `permissionLevel` | string |  |
| `points` | string |  |
| `priority` | string |  |
| `project.access` | boolean |  |
| `project.hidden` | boolean |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `sharing.public` | boolean |  |
| `sharing.publicFields[]` | string |  |
| `sharing.publicShareExpiresOn` | object |  |
| `sharing.seoOptimized` | boolean |  |
| `sharing.token` | object |  |
| `space.id` | string |  |
| `startDate` | string |  |
| `status.color` | string |  |
| `status.id` | string |  |
| `status.orderindex` | number |  |
| `status.status` | string |  |
| `status.type` | string |  |
| `subtasks[].archived` | boolean |  |
| `subtasks[].creator.color` | string |  |
| `subtasks[].creator.email` | string |  |
| `subtasks[].creator.id` | number |  |
| `subtasks[].creator.profilePicture` | object |  |
| `subtasks[].creator.username` | string |  |
| `subtasks[].customItemId` | number |  |
| `subtasks[].dateClosed` | string |  |
| `subtasks[].dateCreated` | string |  |
| `subtasks[].dateDone` | string |  |
| `subtasks[].dateUpdated` | string |  |
| `subtasks[].dueDate` | string |  |
| `subtasks[].id` | string |  |
| `subtasks[].name` | string |  |
| `subtasks[].orderindex` | string |  |
| `subtasks[].parent` | string |  |
| `subtasks[].points` | string |  |
| `subtasks[].startDate` | string |  |
| `subtasks[].status.color` | string |  |
| `subtasks[].status.orderindex` | number |  |
| `subtasks[].status.status` | string |  |
| `subtasks[].status.type` | string |  |
| `subtasks[].timeEstimate` | string |  |
| `subtasks[].timeSpent` | number |  |
| `subtasks[].topLevelParent` | string |  |
| `subtasks[].url` | string |  |
| `teamId` | string |  |
| `textContent` | string |  |
| `timeEstimate` | string |  |
| `timeSpent` | number |  |
| `topLevelParent` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET task/:task_id` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

