# Insighto.ai: List Widgets



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-widgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-widgets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-widgets?${params}`, {
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
      "action_buttons": [
        {}
      ],
      "action_buttons_color": "string",
      "assistant_id": "string",
      "attributes": {},
      "bot_icon_color": "string",
      "bot_message_color": "string",
      "bot_text_message_color": "string",
      "bubble_bot_icon": "string",
      "bubble_color": "string",
      "bubble_text": "string",
      "conversation_bot_icon": "string",
      "description": "string",
      "display_name": "Ava Chen",
      "header_color": "string",
      "header_text_color": "string",
      "ice_break_color": "string",
      "id": "string",
      "intro_message": "string",
      "name": "Ava Chen",
      "org_id": "string",
      "provider_user_friendly_label": "string",
      "remove_branding": true,
      "style_params": {},
      "textbox_default_text": "string",
      "user_message_color": "string",
      "user_opening_messages": [
        "string"
      ],
      "user_text_message_color": "string",
      "widget_provider": "string",
      "widget_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_buttons` | array<object> |  |
| `action_buttons_color` | string |  |
| `assistant_id` | string |  |
| `attributes` | object |  |
| `bot_icon_color` | string |  |
| `bot_message_color` | string |  |
| `bot_text_message_color` | string |  |
| `bubble_bot_icon` | string |  |
| `bubble_color` | string |  |
| `bubble_text` | string |  |
| `conversation_bot_icon` | string |  |
| `description` | string |  |
| `display_name` | string |  |
| `header_color` | string |  |
| `header_text_color` | string |  |
| `ice_break_color` | string |  |
| `id` | string |  |
| `intro_message` | string |  |
| `name` | string |  |
| `org_id` | string |  |
| `provider_user_friendly_label` | string |  |
| `remove_branding` | boolean |  |
| `style_params` | object |  |
| `textbox_default_text` | string |  |
| `user_message_color` | string |  |
| `user_opening_messages` | array<string> |  |
| `user_text_message_color` | string |  |
| `widget_provider` | string |  |
| `widget_type` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `GET /widget` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-widgets.md) for the provider-specific parameters and requirements.

