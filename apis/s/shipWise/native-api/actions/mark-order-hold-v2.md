# Mark Order Hold V2 with ShipWise

Updates an order to hold status in ShipWise.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/Order/:id/Hold`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Mark Order Hold V2](https://api.shipwise.com/swagger/v2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ShipWise order ID. |
