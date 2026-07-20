# Fluents: Get Agent

Retrieves an agent from your Fluents account.

```
GET https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-agent?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-agent?${params}`, {
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
| `id` | string | yes | Fluents agent ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "ask_if_human_present_on_idle": true,
      "call_duration_sec": 1,
      "context_endpoint": "string",
      "conversation_speed": 1,
      "description": "string",
      "enable_dynamic_turns": true,
      "endpointing_sensitivity": "string",
      "id": "string",
      "idle_time_seconds": 1,
      "initial_message": "string",
      "initial_message_delay": 1,
      "interrupt_sensitivity": "string",
      "label": "string",
      "language": "string",
      "llm_temperature": 1,
      "max_idle_check_count": 1,
      "name": "Ava Chen",
      "noise_suppression": true,
      "post_call_actions": [
        {}
      ],
      "post_call_insights": [
        {}
      ],
      "prompt": {},
      "provider": "string",
      "transcriber": {},
      "user_id": "string",
      "voice": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `ask_if_human_present_on_idle` | boolean |  |
| `call_duration_sec` | number |  |
| `context_endpoint` | string |  |
| `conversation_speed` | number |  |
| `description` | string |  |
| `enable_dynamic_turns` | boolean |  |
| `endpointing_sensitivity` | string |  |
| `id` | string |  |
| `idle_time_seconds` | number |  |
| `initial_message` | string |  |
| `initial_message_delay` | number |  |
| `interrupt_sensitivity` | string |  |
| `label` | string |  |
| `language` | string |  |
| `llm_temperature` | number |  |
| `max_idle_check_count` | number |  |
| `name` | string |  |
| `noise_suppression` | boolean |  |
| `post_call_actions` | array<object> |  |
| `post_call_insights` | array<object> |  |
| `prompt` | object |  |
| `provider` | string |  |
| `transcriber` | object |  |
| `user_id` | string |  |
| `voice` | object |  |

## Native endpoint

Through the native Fluents API, this operation is `GET /agents` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

