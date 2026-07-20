# Get Post Processing Label V1 with ShipWise

Retrieves a post-processing label from ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/Print/PostProcessing/:token`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Get Post Processing Label V1](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | path | `string` | yes | Post-processing token returned by a shipment request. |
