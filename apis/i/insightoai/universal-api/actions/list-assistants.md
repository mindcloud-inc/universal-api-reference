# Insighto.ai: List Assistants



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-assistants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-assistants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-assistants?${params}`, {
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

Through the native Insighto.ai API, this operation is `GET /assistant` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assistants.md) for the provider-specific parameters and requirements.

