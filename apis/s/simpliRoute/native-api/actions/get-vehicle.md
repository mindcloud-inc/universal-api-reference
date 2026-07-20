# Get Vehicle with SimpliRoute

Retrieves a vehicle from SimpliRoute by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/routes/vehicles/:vehicle_id/`
- **Base URL:** `https://api.simpliroute.com`
- **Official documentation:** [Get Vehicle](https://documentation.simpliroute.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_extra_properties` | query | `boolean` | no | When true, include the extraProperties object in the response. |
| `vehicle_id` | path | `number` | yes | The SimpliRoute vehicle ID. |
