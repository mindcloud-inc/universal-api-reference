# Get order count with ShopWired

Retrieves the total order count from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/count`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [Get order count](https://shopwired.readme.io/reference/getordercount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `number` | no | Specify 0 for non-archived orders, 1 for archived orders. |
| `status` | query | `number` | no | The ID of the order status. |
| `from` | query | `string` | no | Count orders created after this UNIX timestamp. |
| `to` | query | `string` | no | Count orders created before this UNIX timestamp. |
