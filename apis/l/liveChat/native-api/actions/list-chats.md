# List Chats with LiveChat

Retrieves accessible chat summaries from LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/list_chats`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [List Chats](https://platform.text.com/docs/messaging/agent-chat-api#list-chats)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Filter options remembered across paginated requests. |
| `filters.active` | body | `boolean` | no | Return active chats only when true, inactive chats only when false. |
| `filters.include_chats_without_threads` | body | `boolean` | no | Include chats without any threads in the returned summary. Default true. |
| `filters.group_ids[]` | body | `array<number>` | no | Filter by group IDs. Maximum 200 values. |
| `sort_order` | body | `string` | no | Return oldest chats first with asc or newest chats first with desc. Default desc. |
