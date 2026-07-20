# Get Order Regulated Info with Amazon Seller

Retrieves regulated information for an Amazon Seller order.

## Endpoint

- **Method:** `GET`
- **Path:** `orders/v0/orders/:orderId/regulatedInfo`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Order Regulated Info](https://developer-docs.amazon.com/sp-api/reference/getorderregulatedinfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The Amazon order identifier in 3-7-7 format. |
