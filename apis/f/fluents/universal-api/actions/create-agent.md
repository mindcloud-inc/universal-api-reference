# Fluents: Create Agent

Creates a new agent in Fluents.

```
POST https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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
      "context_endpoint": "string",
      "conversation_speed": 1,
      "deepgram_keywords": {},
      "description": "string",
      "enable_recording": true,
      "endpointing_sensitivity": "string",
      "id": "string",
      "idle_time_seconds": 1,
      "initial_message": "string",
      "initial_message_delay": 1,
      "interrupt_sensitivity": "string",
      "ivr_navigation_mode": "string",
      "label": "string",
      "language": "string",
      "llm_fallback": {},
      "llm_temperature": 1,
      "model": "string",
      "name": "Ava Chen",
      "noise_suppression": true,
      "openai_account_connection": "string",
      "post_call_actions": [
        {}
      ],
      "post_call_insights": [
        {}
      ],
      "prompt": {},
      "provider": "string",
      "run_do_not_call_detection": true,
      "user_id": "string",
      "voice": {},
      "webhook": {}
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
| `context_endpoint` | string |  |
| `conversation_speed` | number |  |
| `deepgram_keywords` | object |  |
| `description` | string |  |
| `enable_recording` | boolean |  |
| `endpointing_sensitivity` | string |  |
| `id` | string |  |
| `idle_time_seconds` | number |  |
| `initial_message` | string |  |
| `initial_message_delay` | number |  |
| `interrupt_sensitivity` | string |  |
| `ivr_navigation_mode` | string |  |
| `label` | string |  |
| `language` | string |  |
| `llm_fallback` | object |  |
| `llm_temperature` | number |  |
| `model` | string |  |
| `name` | string |  |
| `noise_suppression` | boolean |  |
| `openai_account_connection` | string |  |
| `post_call_actions` | array<object> |  |
| `post_call_insights` | array<object> |  |
| `prompt` | object |  |
| `provider` | string |  |
| `run_do_not_call_detection` | boolean |  |
| `user_id` | string |  |
| `voice` | object |  |
| `webhook` | object |  |

## Native endpoint

Through the native Fluents API, this operation is `POST /agents/create` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

