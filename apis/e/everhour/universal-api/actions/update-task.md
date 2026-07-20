# Everhour: Update Task

Updates an existing task in Everhour.

```
PUT https://connect.mindcloud.co/v1/universal/everhour/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "name": "Ava Chen",
  "section": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everhour/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "name": "Ava Chen",
    "section": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Everhour task ID. |
| `name` | string | yes | Task name. |
| `section` | number | yes | Section ID within the project. |
| `labels[]` | array<string> | no | Task labels. |
| `position` | number | no | Task position in the section. |
| `description` | string | no | Task description. |
| `dueOn` | string | no | Due date in YYYY-MM-DD format. |
| `status` | string | no | Task status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
      "comments": 1,
      "completed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "description": "string",
      "favorite": true,
      "id": "string",
      "labels": [
        {}
      ],
      "name": "Ava Chen",
      "position": 1,
      "projects": [
        "string"
      ],
      "section": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> |  |
| `comments` | number |  |
| `completed` | boolean |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `description` | string |  |
| `favorite` | boolean |  |
| `id` | string |  |
| `labels` | array<object> |  |
| `name` | string |  |
| `position` | number |  |
| `projects` | array<string> |  |
| `section` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Everhour API, this operation is `PUT /tasks/:taskId` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

