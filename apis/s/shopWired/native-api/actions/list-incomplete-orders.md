# List incomplete orders with ShopWired

Retrieves incomplete orders from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/incomplete-orders`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [List incomplete orders](https://shopwired.readme.io/reference/listincompleteorders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Return orders created after this UNIX timestamp. |
