# BugHerd: Create Task

Creates a new task in BugHerd.

```
POST https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "511891",
  "task.description": "Found a visual issue on the homepage"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "511891",
    "task.description": "Found a visual issue on the homepage"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | number | yes | Example: `511891`. |
| `task` | object | no |  |
| `task.description` | string | yes | Example: `Found a visual issue on the homepage`. |
| `task.priority` | string | no | Example: `normal`. |
| `task.status` | string | no | Example: `backlog`. |
| `task.assigned_to_id` | number | no | Example: `591329`. |
| `task.requester_email` | string | no | Example: `requester@example.com`. |
| `task.external_id` | string | no | Example: `BUGHERD-TEMP-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminLink` | string |  |
| `assignedTo.avatarUrl` | string |  |
| `assignedTo.displayName` | string |  |
| `assignedTo.email` | string |  |
| `assignedTo.id` | number |  |
| `assignees[].avatarUrl` | string |  |
| `assignees[].displayName` | string |  |
| `assignees[].email` | string |  |
| `assignees[].id` | number |  |
| `closedAt` | object |  |
| `columnId` | number |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `description` | string |  |
| `dueAt` | object |  |
| `externalId` | string |  |
| `fullstorySessionUrl` | object |  |
| `id` | number |  |
| `localTaskId` | number |  |
| `logrocketSessionUrl` | object |  |
| `logs` | object |  |
| `metadata` | object |  |
| `priority` | string |  |
| `priorityId` | number |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `requester` | object |  |
| `requesterBrowser` | object |  |
| `requesterBrowserSize` | object |  |
| `requesterEmail` | string |  |
| `requesterOs` | object |  |
| `requesterResolution` | object |  |
| `screenshotData` | object |  |
| `screenshotUrl` | object |  |
| `secretLink` | string |  |
| `site` | object |  |
| `status` | string |  |
| `statusId` | number |  |
| `title` | object |  |
| `updatedAt` | string |  |
| `updater` | object |  |
| `url` | object |  |

## Native endpoint

Through the native BugHerd API, this operation is `POST projects/:project_id/tasks.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

