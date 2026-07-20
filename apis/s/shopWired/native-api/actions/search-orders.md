# Search for orders with ShopWired

Finds orders in ShopWired by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/search`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [Search for orders](https://shopwired.readme.io/reference/searchorders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords` | query | `string` | no | Keyword(s) to search for, such as order reference or customer name. |
| `session_id` | query | `number` | no | Ensures consistent search results in subsequent calls. |
