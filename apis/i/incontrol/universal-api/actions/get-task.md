# Incontrol: Get Task

Retrieves details for a task from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | The task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closed": "2026-05-07T12:00:00.000Z",
      "dateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "document": {},
      "drafts": [
        {}
      ],
      "finished": "2026-05-07T12:00:00.000Z",
      "form": {},
      "id": "string",
      "name": "Ava Chen",
      "opened": "2026-05-07T12:00:00.000Z",
      "organization": {},
      "reminderAfter": "2026-05-07T12:00:00.000Z",
      "reminderBefore": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | date |  |
| `dateTime` | date |  |
| `description` | string |  |
| `document` | object |  |
| `drafts` | array<object> |  |
| `finished` | date |  |
| `form` | object |  |
| `id` | string |  |
| `name` | string |  |
| `opened` | date |  |
| `organization` | object |  |
| `reminderAfter` | date |  |
| `reminderBefore` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/task/{{id}}` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

