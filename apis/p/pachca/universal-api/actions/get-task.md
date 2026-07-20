# Pachca: Get task



```
GET https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-task?${params}`, {
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
| `id` | number | yes | Pachca task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_id": 1,
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "done_at": "2026-05-07T12:00:00.000Z",
      "due_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "kind": "string",
      "priority": 1,
      "status": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_id` | number |  |
| `content` | string |  |
| `created_at` | date |  |
| `done_at` | date |  |
| `due_at` | date |  |
| `id` | number |  |
| `kind` | string |  |
| `priority` | number |  |
| `status` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Pachca API, this operation is `GET /tasks/{id}` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

