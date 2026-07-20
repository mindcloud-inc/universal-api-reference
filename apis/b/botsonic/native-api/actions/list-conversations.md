# List Conversations with Botsonic

Retrieves all bot conversations from Botsonic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/business/bot-data/conversations/all`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [List Conversations](https://docs.botsonic.com/reference/get_all_conversations_v1_business_bot_data_conversations_all_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | no | Search for conversations matching a query. |
| `sort_by` | query | `string` | no | Conversation type to sort by. |
| `sort_order` | query | `string` | no | Sort direction for conversations. |
| `updated_after` | query | `date` | no | Filter conversations updated after this ISO 8601 datetime. |
| `updated_before` | query | `date` | no | Filter conversations updated before this ISO 8601 datetime. |
