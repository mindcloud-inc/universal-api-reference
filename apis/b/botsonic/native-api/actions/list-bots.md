# List Bots with Botsonic

Retrieves all bots in Botsonic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/business/bot/all`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [List Bots](https://docs.botsonic.com/reference/get_all_bots_v1_business_bot_all_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | no | Optional bot search query. |
| `sort_by` | query | `string` | no | Bot field to sort by. |
| `sort_order` | query | `string` | no | Sort direction. |
| `workspace_id` | query | `string` | no | Optional workspace identifier. |
