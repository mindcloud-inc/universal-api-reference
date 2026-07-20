# Unvoid Shipment V1 with ShipWise

Restores a voided shipment in ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/Ship/:id/UnVoid`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Unvoid Shipment V1](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ShipWise shipment ID. |
