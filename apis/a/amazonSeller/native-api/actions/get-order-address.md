# Get Order Address with Amazon Seller

Retrieves an order shipping address from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `orders/v0/orders/:orderId/address`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Order Address](https://developer-docs.amazon.com/sp-api/reference/getorderaddress)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The Amazon order identifier in 3-7-7 format. |
