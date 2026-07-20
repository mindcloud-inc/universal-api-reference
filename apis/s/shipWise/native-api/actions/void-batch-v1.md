# Void Batch V1 with ShipWise

Voids a batch in ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/Batch/:id/Void`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Void Batch V1](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ShipWise batch ID. |
