# Rate Order Package V1 with ShipWise

Retrieves rates for an order package in ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/Rate/:orderId`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Rate Order Package V1](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | ShipWise order ID. |
