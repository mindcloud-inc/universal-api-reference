# BugHerd: List Feedback Tasks

Retrieves feedback tasks from a BugHerd project.

```
GET https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-feedback-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-feedback-tasks?connectionId=$CONNECTION_ID&project_id=511891" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "511891"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-feedback-tasks?${params}`, {
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
| `project_id` | number | yes | Example: `511891`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToId": 1,
      "assigneeIds": [
        1
      ],
      "closedAt": "2026-05-07T12:00:00.000Z",
      "columnId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dueAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": 1,
      "localTaskId": 1,
      "priorityId": 1,
      "projectId": 1,
      "requesterEmail": "ava@example.com",
      "requesterId": 1,
      "status": "string",
      "statusId": 1,
      "tagNames": [
        "Ava Chen"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToId` | number |  |
| `assigneeIds[]` | number |  |
| `closedAt` | date |  |
| `columnId` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `dueAt` | date |  |
| `externalId` | string |  |
| `id` | number |  |
| `localTaskId` | number |  |
| `priorityId` | number |  |
| `projectId` | number |  |
| `requesterEmail` | string |  |
| `requesterId` | number |  |
| `status` | string |  |
| `statusId` | number |  |
| `tagNames[]` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native BugHerd API, this operation is `GET projects/:project_id/tasks/feedback.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feedback-tasks.md) for the provider-specific parameters and requirements.

