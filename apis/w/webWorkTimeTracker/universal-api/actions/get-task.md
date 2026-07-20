# WebWork Time Tracker: Get Task

Retrieves a task from WebWork Time Tracker.

```
GET https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=1&workspaceId=1&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1",
  "workspaceId": "1",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-task?${params}`, {
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
| `taskId` | number | yes |  |
| `workspaceId` | number | yes |  |
| `projectId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": 1,
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "ownerId": 1,
      "parentId": 1,
      "priority": 1,
      "priorityName": "Ava Chen",
      "projectId": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "statusColor": "string",
      "statusName": "Ava Chen",
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
| `completedAt` | date |  |
| `createdAt` | date |  |
| `creatorId` | number |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `endDate` | date |  |
| `id` | number |  |
| `ownerId` | number |  |
| `parentId` | number |  |
| `priority` | number |  |
| `priorityName` | string |  |
| `projectId` | number |  |
| `startDate` | date |  |
| `status` | number |  |
| `statusColor` | string |  |
| `statusName` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `GET /tasks/:taskId` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

