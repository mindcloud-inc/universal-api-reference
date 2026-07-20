# Query Shipments with ShipWise

Finds shipments in ShipWise by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Ship/Query`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Query Shipments](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `department` | body | `string` | no | Optional department criterion for shipment queries. |
| `shippingProfileId` | body | `string` | no | Optional shipping profile ID criterion for shipment queries. |
| `marketIds` | body | `string` | no | Send multiple values as a array. |
