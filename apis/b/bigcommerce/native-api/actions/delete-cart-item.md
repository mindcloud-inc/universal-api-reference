# Delete Cart Item with BigCommerce

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/carts/:cartId/items/:itemId`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`
- **Official documentation:** [Delete Cart Item](https://developer.bigcommerce.com/docs/rest-management/carts/items#delete-cart-line-item)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cartId` | path | `string` | yes |
| `itemId` | path | `string` | yes |
