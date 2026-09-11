# Get Order Shipping Addresses with BigCommerce

Gets the shipping addresses in an order

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/orders/:orderId/shipping_addresses`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | no | The ID of the order |
