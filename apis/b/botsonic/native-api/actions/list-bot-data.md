# List Bot Data with Botsonic

Retrieves bot data from Botsonic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/business/bot-data/all`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [List Bot Data](https://docs.botsonic.com/reference/get_all_bot_data_v1_business_bot_data_all_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | no | Search for bot data matching a query. |
| `sort_by` | query | `string` | no | Bot data attribute to sort by. |
| `sort_order` | query | `string` | no | Sort direction for bot data results. |
