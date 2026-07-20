# List orders with ShopWired

Retrieves orders from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [List orders](https://shopwired.readme.io/reference/listorders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `list<number>` | no | Comma-separated list of specific order IDs to return, maximum 50. Send multiple values as a string separated by `,`. |
| `archived` | query | `number` | no | Specify 0 for non-archived orders, 1 for archived orders. |
| `status` | query | `number` | no | The ID of the order status. |
| `from` | query | `string` | no | Return orders created after this UNIX timestamp. |
| `to` | query | `string` | no | Return orders created before this UNIX timestamp. |
