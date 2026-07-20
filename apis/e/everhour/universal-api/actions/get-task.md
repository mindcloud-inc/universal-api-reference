# Everhour: Get Task

Retrieves a specific task from Everhour.

```
GET https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | Everhour task ID. |

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

Through the native Everhour API, this operation is `GET /tasks/:taskId` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

