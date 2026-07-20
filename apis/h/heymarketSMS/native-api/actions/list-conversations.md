# List Conversations with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [List Conversations](https://heymarket.docs.apiary.io/api-description-document)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | User ID used to validate inbox access. |
| `filters` | body | `object` | yes | Conversation filters. |
| `inboxes[]` | body | `array<number>` | yes | Inbox IDs to include. |
| `closed` | body | `boolean` | no | Filter by closed conversations. |
| `unread` | body | `boolean` | no | Filter by unread conversations for the given user. |
| `date` | body | `date` | no | Last updated timestamp for pagination. |
