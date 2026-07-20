# Locu: Get Task

Retrieves a single task by ID from Locu.

```
GET https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | Task ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeHtml` | boolean | no | Include description content as HTML |
| `includeMarkdown` | boolean | no | Include description content as Markdown |
| `includePlainText` | boolean | no | Include description content as plain text |
| `includeJson` | boolean | no | Include description content as structured JSON |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "done": "string",
      "doneAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "integrationId": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "section": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Task creation timestamp |
| `done` | string | Task completion state |
| `doneAt` | date | Task completion timestamp |
| `id` | string | Task ID |
| `integrationId` | string | Linked integration ID |
| `name` | string | Task name |
| `projectId` | string | Assigned project ID |
| `section` | string | Task section |
| `type` | string | Task type |

## Native endpoint

Through the native Locu API, this operation is `GET /tasks/:id` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

