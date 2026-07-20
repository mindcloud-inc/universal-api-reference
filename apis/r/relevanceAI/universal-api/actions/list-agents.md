# Relevance AI: List Agents



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agents?${params}`, {
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
| `pageSize` | number | no | Maximum number of agents to return. The official SDK defaults to 20 when omitted. Default: `20`. |
| `page` | number | no | Page number to return. The official SDK defaults to 1 when omitted. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "action_behaviour": "string",
      "active_version_id": "string",
      "agent_id": "string",
      "autonomy_limit": 1,
      "autonomy_limit_behaviour": "string",
      "custom_metadata": {
        "read_metadata_system_prompt": "string",
        "system_prompt": "string"
      },
      "enable_python_executor": true,
      "insert_date_": "2026-05-07T12:00:00.000Z",
      "is_scheduled_triggers_enabled": true,
      "last_updated_by": {
        "user_name": "Ava Chen"
      },
      "machine_user_id": "string",
      "model": "string",
      "name": "Ava Chen",
      "project": "string",
      "public": true,
      "share_styles": {
        "bubble_icon": "string",
        "bubble_style": "string",
        "hide_conversation_list": true,
        "hide_description": true,
        "hide_file_uploads": true,
        "hide_logo": true,
        "hide_tool_steps": true,
        "input_placeholder_text": "string",
        "primary_color": "string",
        "selected_format": "string"
      },
      "suggest_replies": true,
      "system_prompt": "string",
      "temperature": 1,
      "type": "string",
      "update_date_": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `action_behaviour` | string |  |
| `active_version_id` | string |  |
| `agent_id` | string |  |
| `autonomy_limit` | number |  |
| `autonomy_limit_behaviour` | string |  |
| `custom_metadata.read_metadata_system_prompt` | string |  |
| `custom_metadata.system_prompt` | string |  |
| `enable_python_executor` | boolean |  |
| `insert_date_` | date |  |
| `is_scheduled_triggers_enabled` | boolean |  |
| `last_updated_by.user_name` | string |  |
| `machine_user_id` | string |  |
| `model` | string |  |
| `name` | string |  |
| `project` | string |  |
| `public` | boolean |  |
| `share_styles.bubble_icon` | string |  |
| `share_styles.bubble_style` | string |  |
| `share_styles.hide_conversation_list` | boolean |  |
| `share_styles.hide_description` | boolean |  |
| `share_styles.hide_file_uploads` | boolean |  |
| `share_styles.hide_logo` | boolean |  |
| `share_styles.hide_tool_steps` | boolean |  |
| `share_styles.input_placeholder_text` | string |  |
| `share_styles.primary_color` | string |  |
| `share_styles.selected_format` | string |  |
| `suggest_replies` | boolean |  |
| `system_prompt` | string |  |
| `temperature` | number |  |
| `type` | string |  |
| `update_date_` | date |  |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /agents/list` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

