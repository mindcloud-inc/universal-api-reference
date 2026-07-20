# List Agents For Transfer with LiveChat

Retrieves agents available for chat transfer in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/list_agents_for_transfer`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [List Agents For Transfer](https://platform.text.com/docs/messaging/agent-chat-api#list-agents-for-transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The chat ID to inspect for transfer targets. |
