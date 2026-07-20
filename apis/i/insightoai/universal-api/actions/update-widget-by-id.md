# Insighto.ai: Update Widget By Id



```
PUT https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/update-widget-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/update-widget-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "widgetId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
  "widgetType": "chat"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/update-widget-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "widgetId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
    "widgetType": "chat"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `widgetId` | string | yes | The UUID id of the widget. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |
| `widgetType` | list<string> | yes | Widget type to update. One of: `chat`, `fb_messenger`, `html`, `html_call`, `instagram`, `leadconnector`, `leadconnector_call`, `phone`, `plivo_call`, `render_form`, `sip`, `sms`, `telegram`, `telnyx_call`, `web_call`, `whatsapp`. Example: `chat`. |
| `userOpeningMessages[]` | array<string> | no | Opening messages shown to users. Example: `Need help?`. |
| `actionButtons[]` | array<object> | no | Action buttons shown in the widget. |
| `name` | string | no | Widget name. Example: `Support Widget Updated`. |

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

Through the native Insighto.ai API, this operation is `PUT /widget/:widget_id` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-widget-by-id.md) for the provider-specific parameters and requirements.

