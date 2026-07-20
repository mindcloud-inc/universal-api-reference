# DoneDone: Get Task

Retrieves a task from DoneDone.

```
GET https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-task?connectionId=$CONNECTION_ID&accountId=1&projectId=1&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "projectId": "1",
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-task?${params}`, {
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
| `accountId` | number | yes | DoneDone account ID. |
| `projectId` | number | yes | DoneDone internal project ID. |
| `taskId` | number | yes | DoneDone task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessEpochTime": "2026-05-07T12:00:00.000Z",
      "assignee": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "creator": {
        "email": "ava@example.com",
        "id": 1,
        "isGuest": true,
        "name": "Ava Chen",
        "photoUrl": "https://example.com"
      },
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "harvestEnabled": true,
      "id": 1,
      "isPinned": true,
      "priority": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "project": {
        "id": 1,
        "name": "Ava Chen"
      },
      "refNumber": 1,
      "status": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessEpochTime` | date |  |
| `assignee` | object |  |
| `createdOn` | date |  |
| `creator.email` | string |  |
| `creator.id` | number |  |
| `creator.isGuest` | boolean |  |
| `creator.name` | string |  |
| `creator.photoUrl` | string |  |
| `description` | string |  |
| `dueDate` | date |  |
| `harvestEnabled` | boolean |  |
| `id` | number |  |
| `isPinned` | boolean |  |
| `priority.color` | string |  |
| `priority.id` | number |  |
| `priority.name` | string |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `refNumber` | number |  |
| `status.color` | string |  |
| `status.id` | number |  |
| `status.name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native DoneDone API, this operation is `GET /:account_id/internal-projects/:internal_project_id/tasks/:task_id` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

