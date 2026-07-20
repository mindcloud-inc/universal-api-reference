# Pachca (Admin): Get Task

Retrieves a task from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-task?${params}`, {
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
| `id` | number | yes | The Pachca task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "allDay": true,
        "chatId": 1,
        "content": "string",
        "createdAt": "string",
        "dueAt": {},
        "id": 1,
        "kind": "string",
        "performerIds": [
          1
        ],
        "priority": 1,
        "status": "string",
        "userId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.allDay` | boolean |  |
| `data.chatId` | number |  |
| `data.content` | string |  |
| `data.createdAt` | string |  |
| `data.dueAt` | object |  |
| `data.id` | number |  |
| `data.kind` | string |  |
| `data.performerIds[]` | number |  |
| `data.priority` | number |  |
| `data.status` | string |  |
| `data.userId` | number |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /tasks/:id` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

