# List Routing Statuses with LiveChat

Retrieves agent routing statuses from LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/list_routing_statuses`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [List Routing Statuses](https://platform.text.com/docs/messaging/agent-chat-api#list-routing-statuses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Routing status filters. |
| `filters.group_ids[]` | body | `array<number>` | no | Filter statuses by group IDs. |
