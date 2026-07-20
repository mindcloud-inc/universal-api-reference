# Mark Order New V2 with ShipWise

Updates an order to new status in ShipWise.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/Order/:id/New`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Mark Order New V2](https://api.shipwise.com/swagger/v2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ShipWise order ID. |
