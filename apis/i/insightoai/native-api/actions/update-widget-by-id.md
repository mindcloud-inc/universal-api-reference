# Update Widget By Id with Insighto.ai

## Endpoint

- **Method:** `PUT`
- **Path:** `/widget/:widget_id`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Update Widget By Id](https://docs.insighto.ai/api-reference/widget/update-widget-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widget_id` | path | `string` | yes | The UUID id of the widget. |
| `widget_type` | body | `list<string>` | yes | Widget type to update. Accepted values: `chat`, `fb_messenger`, `html`, `html_call`, `instagram`, `leadconnector`, `leadconnector_call`, `phone`, `plivo_call`, `render_form`, `sip`, `sms`, `telegram`, `telnyx_call`, `web_call`, `whatsapp`. |
| `user_opening_messages[]` | body | `array<string>` | no | Opening messages shown to users. |
| `action_buttons[]` | body | `array<object>` | no | Action buttons shown in the widget. |
| `name` | body | `string` | no | Widget name. |
