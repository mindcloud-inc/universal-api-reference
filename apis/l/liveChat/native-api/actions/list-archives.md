# List Archives with LiveChat

Retrieves archived chats and thread events from LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/list_archives`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [List Archives](https://platform.text.com/docs/messaging/agent-chat-api#list-archives)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Archive search filters. |
| `filters.query` | body | `string` | no | Free-text archive query. |
| `filters.from` | body | `date` | no | Lower RFC3339 timestamp bound for archives. |
| `filters.to` | body | `date` | no | Upper RFC3339 timestamp bound for archives. |
| `filters.chat_ids[]` | body | `array<string>` | no | Filter by chat IDs. |
| `filters.thread_ids[]` | body | `array<string>` | no | Filter by thread IDs. |
| `filters.group_ids[]` | body | `array<number>` | no | Filter by group IDs. |
| `filters.customer_id` | body | `string` | no | Filter by customer ID. |
| `filters.customer_email` | body | `string` | no | Filter by customer email. |
| `sort_order` | body | `string` | no | Default desc. |
