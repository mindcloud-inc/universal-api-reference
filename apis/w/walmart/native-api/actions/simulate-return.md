# Simulate Return with Walmart

Simulates the return creation for a given customer order and line item.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/simulations/returns`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Simulate Return](https://developer.walmart.com/us-marketplace/reference/simulatereturn)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderId` | body | `string` | yes | Purchase order identifier for the order being used in the return simulation. |
| `lineNumber` | body | `number` | yes | Line number of an item within the order to return. |
| `qty` | body | `number` | yes | Quantity of units being returned for the specified order line. |
| `returnReason` | body | `list<string>` | yes | Reason for initiating the return. |
