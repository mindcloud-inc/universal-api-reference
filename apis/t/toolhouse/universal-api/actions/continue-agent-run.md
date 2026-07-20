# Toolhouse: Continue Agent Run



```
PUT https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/continue-agent-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toolhouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/continue-agent-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "runId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/continue-agent-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "runId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | The follow-up message to continue the agent run with. |
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

Through the native Toolhouse API, this operation is `PUT /agent-runs/:run_id` (base URL `https://api.toolhouse.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/continue-agent-run.md) for the provider-specific parameters and requirements.

