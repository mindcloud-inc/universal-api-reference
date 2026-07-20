# Toolhouse: Create Agent Run



```
POST https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/create-agent-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toolhouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/create-agent-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/create-agent-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bundle` | string | no | Optional Toolhouse bundle name. |
| `callbackUrl` | string | no | Optional webhook URL to receive completion callbacks. |
| `chatId` | string | yes | The Toolhouse chat ID to run. |
| `toolhouseId` | string | no | Optional Toolhouse workspace identifier. |
| `vars` | object | no | Variables passed to the agent run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bundle": "string",
      "callback_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "id": "string",
      "results": [
        {}
      ],
      "schedule_id": "string",
      "status": "string",
      "toolhouse_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string",
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
| `created_at` | date |  |
| `error` | string |  |
| `id` | string |  |
| `results` | array<object> |  |
| `schedule_id` | string |  |
| `status` | string |  |
| `toolhouse_id` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |
| `vars` | object |  |

## Native endpoint

Through the native Toolhouse API, this operation is `POST /agent-runs` (base URL `https://api.toolhouse.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-run.md) for the provider-specific parameters and requirements.

