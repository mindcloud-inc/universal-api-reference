# Insighto.ai: Create Assistant



```
POST https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/create-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/create-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assistantType": "simple",
  "llmModel": "gpt-4o-mini"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/create-assistant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assistantType": "simple",
    "llmModel": "gpt-4o-mini"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assistantType` | list<string> | yes | Assistant type to create. One of: `chat`, `nl2sql`, `phone`, `realtime_openai`, `simple`. Example: `simple`. |
| `llmModel` | list<string> | yes | Foundation model used by the assistant. One of: `deepseek-r1-distill-llama-70b`, `gpt-3.5-turbo`, `gpt-3.5-turbo-0125`, `gpt-3.5-turbo-1106`, `gpt-4-0125-preview`, `gpt-4-1106-preview`, `gpt-4o-2024-05-13`, `gpt-4o-mini`, `gpt-4o-mini-realtime-preview`, `gpt-4o-realtime-preview`, `llama-3.1-70b-versatile`, `o3-mini`. Example: `gpt-4o-mini`. |
| `name` | string | no | Assistant name. Example: `Support Assistant`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assistant_type": "string",
      "attributes": {},
      "conversation_flow_id": "string",
      "custom_voice": true,
      "description": "string",
      "has_human_agent": true,
      "hide_ds": true,
      "id": "string",
      "llm_model": "string",
      "name": "Ava Chen",
      "org_id": "string",
      "show_images": true,
      "system_prompt": "string",
      "use_tools": true,
      "voice": true,
      "voice_languages": [
        "string"
      ],
      "webhook_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assistant_type` | string |  |
| `attributes` | object |  |
| `conversation_flow_id` | string |  |
| `custom_voice` | boolean |  |
| `description` | string |  |
| `has_human_agent` | boolean |  |
| `hide_ds` | boolean |  |
| `id` | string |  |
| `llm_model` | string |  |
| `name` | string |  |
| `org_id` | string |  |
| `show_images` | boolean |  |
| `system_prompt` | string |  |
| `use_tools` | boolean |  |
| `voice` | boolean |  |
| `voice_languages` | array<string> |  |
| `webhook_id` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `POST /assistant` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-assistant.md) for the provider-specific parameters and requirements.

