# Get Products In Order with BigCommerce

Gets the products listed in the order

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/orders/:orderId/products`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | The ID of the order |
