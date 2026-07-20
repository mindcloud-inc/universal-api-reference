# Toolhouse: Get Agent Run



```
GET https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/get-agent-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toolhouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/get-agent-run?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/get-agent-run?${params}`, {
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
| `runId` | string | yes | The agent run ID. |

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
      "id": "string",
      "last_agent_message": "string",
      "results": [
        {}
      ],
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
| `id` | string |  |
| `last_agent_message` | string |  |
| `results` | array<object> |  |
| `schedule_id` | string |  |
| `status` | string |  |
| `toolhouse_id` | string |  |
| `updated_at` | date |  |
| `vars` | object |  |

## Native endpoint

Through the native Toolhouse API, this operation is `GET /agent-runs/:run_id` (base URL `https://api.toolhouse.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-run.md) for the provider-specific parameters and requirements.

