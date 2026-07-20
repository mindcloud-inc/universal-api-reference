# Get Order Buyer Info with Amazon Seller

Retrieves buyer information for an Amazon Seller order.

## Endpoint

- **Method:** `GET`
- **Path:** `orders/v0/orders/:orderId/buyerInfo`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Order Buyer Info](https://developer-docs.amazon.com/sp-api/reference/getorderbuyerinfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The Amazon order identifier in 3-7-7 format. |
