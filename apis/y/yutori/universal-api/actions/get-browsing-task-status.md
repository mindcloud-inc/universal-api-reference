# Yutori: Get Browsing Task Status

Retrieves the status and results of a Yutori browsing task.

```
GET https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-browsing-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yutori `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-browsing-task-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-browsing-task-status?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paused": true,
      "result": "string",
      "status": "string",
      "structured_output_status": "string",
      "task_id": "string",
      "view_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paused` | boolean |  |
| `result` | string |  |
| `status` | string |  |
| `structured_output_status` | string |  |
| `task_id` | string |  |
| `view_url` | string |  |

## Native endpoint

Through the native Yutori API, this operation is `GET /v1/browsing/tasks/:id` (base URL `https://api.yutori.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-browsing-task-status.md) for the provider-specific parameters and requirements.

