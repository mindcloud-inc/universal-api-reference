# List Orders with SquareSpace

Retrieves orders from Squarespace.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/commerce/orders`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [List Orders](https://developers.squarespace.com/commerce-apis/orders#list-orders)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | query | `string` | no | Filter orders by customer profile ID. |
| `fulfillmentStatus` | query | `list<string>` | no | Filter orders by fulfillment status. Accepted values: `CANCELED`, `FULFILLED`, `PENDING`. |
| `modifiedAfter` | query | `date` | no | Return orders modified after this datetime. |
| `modifiedBefore` | query | `date` | no | Return orders modified before this datetime. |
