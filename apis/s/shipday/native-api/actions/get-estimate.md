# Get Estimate with Shipday

Retrieves an estimate from Shipday for an order.

## Endpoint

- **Method:** `GET`
- **Path:** `/on-demand/estimate/:orderId`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Get Estimate](https://docs.shipday.com/reference/estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Shipday order ID used in the request path. |
