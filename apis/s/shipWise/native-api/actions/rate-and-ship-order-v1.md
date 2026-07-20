# Rate And Ship Order V1 with ShipWise

Rates and ships an order in ShipWise.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Ship/RateAndShip/:orderId`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Rate And Ship Order V1](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | ShipWise order ID. |
