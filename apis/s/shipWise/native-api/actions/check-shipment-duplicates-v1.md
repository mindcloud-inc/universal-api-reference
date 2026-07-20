# Check Shipment Duplicates V1 with ShipWise

Checks for shipment duplicates in ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/Ship/:id/Check`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Check Shipment Duplicates V1](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ShipWise shipment ID. |
