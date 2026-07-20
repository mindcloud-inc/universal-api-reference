# List Orders V2 with ShipWise

Retrieves orders from ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/Order`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [List Orders V2](https://api.shipwise.com/swagger/v2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAtMax` | query | `string` | no | Maximum create date on the orders. |
| `createdAtMin` | query | `string` | no | Minimum create date on the orders. |
