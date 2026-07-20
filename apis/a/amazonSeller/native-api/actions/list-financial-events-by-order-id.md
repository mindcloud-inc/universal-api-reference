# List Financial Events by Order ID with Amazon Seller

Retrieves financial events for an Amazon Seller order.

## Endpoint

- **Method:** `GET`
- **Path:** `finances/v0/orders/:orderId/financialEvents`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [List Financial Events by Order ID](https://developer-docs.amazon.com/sp-api/reference/listfinancialeventsbyorderid)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | An Amazon-defined order identifier, in 3-7-7 format. |
