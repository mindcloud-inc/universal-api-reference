# Create Widget with Insighto.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/widget`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Create Widget](https://docs.insighto.ai/api-reference/widget/create-widget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widget_type` | body | `list<string>` | yes | Widget type to create. Accepted values: `chat`, `fb_messenger`, `html`, `html_call`, `instagram`, `leadconnector`, `leadconnector_call`, `phone`, `plivo_call`, `render_form`, `sip`, `sms`, `telegram`, `telnyx_call`, `web_call`, `whatsapp`. |
| `user_opening_messages[]` | body | `array<string>` | yes | Opening messages shown to users. |
| `action_buttons[]` | body | `array<object>` | yes | Action buttons shown in the widget. |
| `assistant_id` | body | `string` | no | Assistant linked to the widget. |
| `name` | body | `string` | no | Widget name. |
