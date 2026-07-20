# Send WABP Template Message with SeaX

Sends a WhatsApp template message from SeaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/send_message/wabp_template_message`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Send WABP Template Message](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | body | `string` | yes | Conversation identifier. |
| `template_language` | body | `string` | yes | Template language code. |
| `template_name` | body | `string` | yes | Template name. |
