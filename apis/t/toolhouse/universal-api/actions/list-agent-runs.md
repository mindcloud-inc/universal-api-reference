# Toolhouse: List Agent Runs



```
GET https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/list-agent-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toolhouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/list-agent-runs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/list-agent-runs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "bundle": "string",
      "callback_url": "https://example.com",
      "chat_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "id": "string",
      "schedule_id": "string",
      "status": "string",
      "toolhouse_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "vars": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bundle` | string |  |
| `callback_url` | string |  |
| `chat_id` | string |  |
| `created_at` | date |  |
| `error` | string |  |
| `id` | string |  |
| `schedule_id` | string |  |
| `status` | string |  |
| `toolhouse_id` | string |  |
| `updated_at` | date |  |
| `vars` | object |  |

## Native endpoint

Through the native Toolhouse API, this operation is `GET /agent-runs` (base URL `https://api.toolhouse.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-runs.md) for the provider-specific parameters and requirements.

