# BugHerd: Create Comment

Creates a comment on a BugHerd task.

```
POST https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "511891",
  "task_id": "29003679",
  "comment.text": "Looking into this now."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "511891",
    "task_id": "29003679",
    "comment.text": "Looking into this now."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | number | yes | Example: `511891`. |
| `task_id` | number | yes | Example: `29003679`. |
| `comment` | object | no |  |
| `comment.text` | string | yes | Example: `Looking into this now.`. |
| `comment.email` | string | no | Example: `commenter@example.com`. |
| `comment.is_private` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment.user_id` | number | no | Example: `591329`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "deletedAt": {},
      "id": 1,
      "isPrivate": true,
      "task": {
        "adminLink": "https://example.com",
        "assignedTo": {
          "avatarUrl": "https://example.com",
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": 1
        },
        "assignees": [
          {
            "avatarUrl": "https://example.com",
            "displayName": "Ava Chen",
            "email": "ava@example.com",
            "id": 1
          }
        ],
        "closedAt": {},
        "columnId": 1,
        "createdAt": "string",
        "deletedAt": {},
        "description": "string",
        "dueAt": {},
        "externalId": "string",
        "fullstorySessionUrl": {},
        "id": 1,
        "localTaskId": 1,
        "logrocketSessionUrl": {},
        "logs": {},
        "metadata": {},
        "priority": "string",
        "priorityId": 1,
        "projectId": 1,
        "projectName": "Ava Chen",
        "requester": {},
        "requesterBrowser": {},
        "requesterBrowserSize": {},
        "requesterEmail": "ava@example.com",
        "requesterOs": {},
        "requesterResolution": {},
        "screenshotData": {},
        "screenshotUrl": {},
        "secretLink": "https://example.com",
        "site": {},
        "status": "string",
        "statusId": 1,
        "title": {},
        "updatedAt": "string",
        "updater": {},
        "url": {}
      },
      "text": "string",
      "updatedAt": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `id` | number |  |
| `isPrivate` | boolean |  |
| `task.adminLink` | string |  |
| `task.assignedTo.avatarUrl` | string |  |
| `task.assignedTo.displayName` | string |  |
| `task.assignedTo.email` | string |  |
| `task.assignedTo.id` | number |  |
| `task.assignees[].avatarUrl` | string |  |
| `task.assignees[].displayName` | string |  |
| `task.assignees[].email` | string |  |
| `task.assignees[].id` | number |  |
| `task.closedAt` | object |  |
| `task.columnId` | number |  |
| `task.createdAt` | string |  |
| `task.deletedAt` | object |  |
| `task.description` | string |  |
| `task.dueAt` | object |  |
| `task.externalId` | string |  |
| `task.fullstorySessionUrl` | object |  |
| `task.id` | number |  |
| `task.localTaskId` | number |  |
| `task.logrocketSessionUrl` | object |  |
| `task.logs` | object |  |
| `task.metadata` | object |  |
| `task.priority` | string |  |
| `task.priorityId` | number |  |
| `task.projectId` | number |  |
| `task.projectName` | string |  |
| `task.requester` | object |  |
| `task.requesterBrowser` | object |  |
| `task.requesterBrowserSize` | object |  |
| `task.requesterEmail` | string |  |
| `task.requesterOs` | object |  |
| `task.requesterResolution` | object |  |
| `task.screenshotData` | object |  |
| `task.screenshotUrl` | object |  |
| `task.secretLink` | string |  |
| `task.site` | object |  |
| `task.status` | string |  |
| `task.statusId` | number |  |
| `task.title` | object |  |
| `task.updatedAt` | string |  |
| `task.updater` | object |  |
| `task.url` | object |  |
| `text` | string |  |
| `updatedAt` | string |  |
| `user` | object |  |

## Native endpoint

Through the native BugHerd API, this operation is `POST projects/:project_id/tasks/:task_id/comments.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

