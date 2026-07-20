# ClickUp: Update Task



```
PUT https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignees.add[]` | array<number> | no |  |
| `customItemId` | number | no | To convert an item using a custom task type into a task, send 'null'. To update this task to be a Milestone, send a value of 1. To use a custom task type, send the custom task type ID as defined in your Workspace, such as 2. |
| `groupAssignees.add[]` | array<number> | no |  |
| `markdownContent` | string | no |  |
| `watchers.add[]` | array<number> | no |  |
| `assignees.rem[]` | array<number> | no |  |
| `groupAssignees.rem[]` | array<number> | no |  |
| `name` | string | no |  |
| `watchers.rem[]` | array<number> | no |  |
| `description` | string | no |  |
| `status` | string | no |  |
| `priority` | list | no |  |
| `dueDate` | date | no |  |
| `dueDateTime` | boolean | no |  |
| `startDate` | date | no |  |
| `startDateTime` | boolean | no |  |
| `points` | number | no |  |
| `archived` | boolean | no |  |
| `parent` | string | no | You can move a subtask to another parent task by including "parent" with a valid task id. You cannot convert a subtask to a task by setting "parent" to null. |
| `timeEstimate` | number | no | Time in milliseconds |
| `assignees` | object | no |  |
| `groupAssignees` | object | no |  |
| `watchers` | object | no |  |
| `customTaskIds` | boolean | no |  |
| `taskId` | string | yes |  |
| `teamId` | list | no |  |

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
      "customFields": [
        {
          "dateCreated": "string",
          "hideFromGuests": true,
          "id": "string",
          "name": "Ava Chen",
          "required": true,
          "type": "string",
          "typeConfig": {
            "options": [
              {
                "color": {},
                "id": "string",
                "name": "Ava Chen",
                "orderindex": 1
              }
            ],
            "sorting": "string"
          }
        }
      ],
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
      "teamId": "string",
      "textContent": "string",
      "timeEstimate": "string",
      "timeSpent": 1,
      "topLevelParent": "string",
      "url": "https://example.com",
      "watchers": [
        {
          "color": "string",
          "email": "ava@example.com",
          "id": 1,
          "initials": "string",
          "profilePicture": {},
          "username": "Ava Chen"
        }
      ]
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
| `customFields[].dateCreated` | string |  |
| `customFields[].hideFromGuests` | boolean |  |
| `customFields[].id` | string |  |
| `customFields[].name` | string |  |
| `customFields[].required` | boolean |  |
| `customFields[].type` | string |  |
| `customFields[].typeConfig.options[].color` | object |  |
| `customFields[].typeConfig.options[].id` | string |  |
| `customFields[].typeConfig.options[].name` | string |  |
| `customFields[].typeConfig.options[].orderindex` | number |  |
| `customFields[].typeConfig.sorting` | string |  |
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
| `teamId` | string |  |
| `textContent` | string |  |
| `timeEstimate` | string |  |
| `timeSpent` | number |  |
| `topLevelParent` | string |  |
| `url` | string |  |
| `watchers[].color` | string |  |
| `watchers[].email` | string |  |
| `watchers[].id` | number |  |
| `watchers[].initials` | string |  |
| `watchers[].profilePicture` | object |  |
| `watchers[].username` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `PUT task/:task_id` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

