# Update Shipping for Order with BigCommerce

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/orders/:orderId/shipments/:shipmentId`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `string` | yes |
| `shipmentId` | path | `string` | yes |
| `trackingNumber` | body | `string` | no |
