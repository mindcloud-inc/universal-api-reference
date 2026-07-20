# BugHerd: Show Task By Local Task ID

Retrieves a BugHerd task by local task ID.

```
GET https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-task-by-local-task-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-task-by-local-task-id?connectionId=$CONNECTION_ID&local_task_id=1&project_id=511891" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "local_task_id": "1",
  "project_id": "511891"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-task-by-local-task-id?${params}`, {
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
| `local_task_id` | number | yes | Example: `1`. |
| `project_id` | number | yes | Example: `511891`. |

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
      "attachments": [
        {
          "id": 1,
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "closedAt": "2026-05-07T12:00:00.000Z",
      "columnId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dueAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": 1,
      "localTaskId": 1,
      "priority": "string",
      "priorityId": 1,
      "projectId": 1,
      "projectName": "Ava Chen",
      "requesterEmail": "ava@example.com",
      "screenshotUrl": "https://example.com",
      "secretLink": "https://example.com",
      "status": "string",
      "statusId": 1,
      "tagNames": [
        "Ava Chen"
      ],
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `attachments[].id` | number |  |
| `attachments[].name` | string |  |
| `attachments[].url` | string |  |
| `closedAt` | date |  |
| `columnId` | number |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `dueAt` | date |  |
| `externalId` | string |  |
| `id` | number |  |
| `localTaskId` | number |  |
| `priority` | string |  |
| `priorityId` | number |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `requesterEmail` | string |  |
| `screenshotUrl` | string |  |
| `secretLink` | string |  |
| `status` | string |  |
| `statusId` | number |  |
| `tagNames[]` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native BugHerd API, this operation is `GET projects/:project_id/local_tasks/:local_task_id.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-task-by-local-task-id.md) for the provider-specific parameters and requirements.

