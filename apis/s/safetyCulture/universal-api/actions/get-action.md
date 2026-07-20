# SafetyCulture: Get Action

Retrieves an action from SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-action?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-action?${params}`, {
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
| `id` | string | yes | ID to query data for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "task": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "dueAt": "2026-05-07T12:00:00.000Z",
        "priorityId": "string",
        "site": {
          "name": "Ava Chen"
        },
        "status": {
          "label": "string"
        },
        "taskId": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `task.createdAt` | date |  |
| `task.description` | string |  |
| `task.dueAt` | date |  |
| `task.priorityId` | string |  |
| `task.site.name` | string |  |
| `task.status.label` | string |  |
| `task.taskId` | string |  |
| `task.title` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `GET /tasks/v1/actions/{id}` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action.md) for the provider-specific parameters and requirements.

