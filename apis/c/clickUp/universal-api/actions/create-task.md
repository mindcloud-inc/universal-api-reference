# ClickUp: Create Task

Create a new task.

```
POST https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeEstimate` | number | no | Time estimate in milliseconds |
| `customFields[].id` | string | no |  |
| `listId` | string | yes |  |
| `customFields[].value` | string | no |  |
| `customFields[]` | array<object> | no |  |
| `customItemId` | number | no | To create a task that doesn't use a custom task type, either don't include this field in the request body, or send 'null'. To create this task as a Milestone, send a value of 1. To use a custom task type, send the custom task type ID as defined in your Workspace, such as 2. |
| `archived` | boolean | no |  |
| `assignees[]` | array<number> | no |  |
| `checkRequiredCustomFields` | boolean | no | Default: `True`. |
| `description` | string | no |  |
| `dueDate` | date | no |  |
| `dueDateTime` | boolean | no |  |
| `groupAssignees` | array<number> | no |  |
| `linksTo` | string | no |  |
| `markdownContent` | string | no |  |
| `name` | string | yes |  |
| `notifyAll` | boolean | no |  |
| `parent` | string | no |  |
| `points` | number | no |  |
| `priority` | list | no |  |
| `startDate` | date | no |  |
| `startDateTime` | boolean | no |  |
| `status` | string | no |  |
| `tags` | array<string> | no |  |

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
        "profilePicture": "string",
        "username": "Ava Chen"
      },
      "customFields": [
        {
          "name": "Ava Chen",
          "value": "string",
          "dateCreated": 1,
          "hideFromGuests": true,
          "id": "string",
          "required": true,
          "type": "string"
        }
      ],
      "customId": "string",
      "customItemId": 1,
      "dateClosed": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateDone": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
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
      "points": 1,
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
        "publicShareExpiresOn": "2026-05-07T12:00:00.000Z",
        "seoOptimized": true,
        "token": "string"
      },
      "space": {
        "id": "string"
      },
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": {
        "color": "string",
        "id": "string",
        "orderindex": 1,
        "status": "string",
        "type": "string"
      },
      "teamId": "string",
      "textContent": "string",
      "timeEstimate": 1,
      "timeSpent": 1,
      "topLevelParent": "string",
      "url": "https://example.com",
      "watchers": [
        {
          "color": "string",
          "email": "ava@example.com",
          "id": 1,
          "initials": "string",
          "profilePicture": "string",
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
| `creator.profilePicture` | string |  |
| `creator.username` | string |  |
| `customFields` | array |  |
| `customFields[]. name` | string |  |
| `customFields[]. value` | string |  |
| `customFields[].dateCreated` | number |  |
| `customFields[].hideFromGuests` | boolean |  |
| `customFields[].id` | string |  |
| `customFields[].required` | boolean |  |
| `customFields[].type` | string |  |
| `customId` | string |  |
| `customItemId` | number |  |
| `dateClosed` | date |  |
| `dateCreated` | date |  |
| `dateDone` | date |  |
| `dateUpdated` | date |  |
| `description` | string |  |
| `dueDate` | date |  |
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
| `points` | number |  |
| `priority` | string |  |
| `project.access` | boolean |  |
| `project.hidden` | boolean |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `sharing.public` | boolean |  |
| `sharing.publicFields[]` | string |  |
| `sharing.publicShareExpiresOn` | date |  |
| `sharing.seoOptimized` | boolean |  |
| `sharing.token` | string |  |
| `space.id` | string |  |
| `startDate` | date |  |
| `status.color` | string |  |
| `status.id` | string |  |
| `status.orderindex` | number |  |
| `status.status` | string |  |
| `status.type` | string |  |
| `teamId` | string |  |
| `textContent` | string |  |
| `timeEstimate` | number |  |
| `timeSpent` | number |  |
| `topLevelParent` | string |  |
| `url` | string |  |
| `watchers[].color` | string |  |
| `watchers[].email` | string |  |
| `watchers[].id` | number |  |
| `watchers[].initials` | string |  |
| `watchers[].profilePicture` | string |  |
| `watchers[].username` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `POST list/:list_id/task` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

