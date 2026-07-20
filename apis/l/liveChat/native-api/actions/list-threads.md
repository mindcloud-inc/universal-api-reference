# List Threads with LiveChat

Retrieves accessible chat threads from LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/list_threads`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [List Threads](https://platform.text.com/docs/messaging/agent-chat-api#list-threads)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The ID of the chat. |
| `sort_order` | body | `string` | no | Return oldest threads first with asc or newest threads first with desc. Default desc. |
| `min_events_count` | body | `number` | no | Minimum total number of events to return across the latest threads. |
| `filters` | body | `object` | no | Date range filters for the listed threads. |
| `filters.from` | body | `date` | no | Lower RFC3339 timestamp bound for returned threads. |
| `filters.to` | body | `date` | no | Upper RFC3339 timestamp bound for returned threads. |
