# Void Shipment V1 with ShipWise

Voids a shipment in ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/Ship/:id/Void`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Void Shipment V1](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ShipWise shipment ID. |
