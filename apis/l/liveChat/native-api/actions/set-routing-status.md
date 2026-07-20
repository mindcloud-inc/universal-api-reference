# Set Routing Status with LiveChat

Updates an agent routing status in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/set_routing_status`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Set Routing Status](https://platform.text.com/docs/messaging/agent-chat-api#set-routing-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | body | `string` | yes | Routing status to apply. |
| `agent_id` | body | `string` | no | The agent ID to update. Defaults to the requester when omitted. |
