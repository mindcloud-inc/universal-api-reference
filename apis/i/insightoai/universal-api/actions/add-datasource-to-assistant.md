# Insighto.ai: Add Datasource To Assistant



```
PUT https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-datasource-to-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-datasource-to-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assistantId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
  "datasourceId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-datasource-to-assistant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assistantId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
    "datasourceId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assistantId` | string | yes | The UUID id of the assistant. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |
| `datasourceId` | string | yes | The UUID id of the datasource. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |

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

Through the native Insighto.ai API, this operation is `POST /assistant/:assistant_id/data_source/:datasource_id` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-datasource-to-assistant.md) for the provider-specific parameters and requirements.

