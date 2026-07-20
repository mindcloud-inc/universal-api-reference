# List Conversations with Insighto.ai

## Endpoint

- **Method:** `GET`
- **Path:** `/conversation`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [List Conversations](https://docs.insighto.ai/api-reference/conversation/get-list-of-conversations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | yes | Start date in ISO format (YYYY-MM-DD). |
| `date_to` | query | `string` | yes | End date in ISO format (YYYY-MM-DD). |
| `assistant_id` | query | `string` | no | Filter conversations by assistant id. |
| `intent_id` | query | `string` | no | Filter conversations by intent id. |
| `includes_voice` | query | `boolean` | no | Whether to include voice conversations. |
