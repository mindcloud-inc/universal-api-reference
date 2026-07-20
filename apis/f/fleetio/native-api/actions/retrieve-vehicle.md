# Retrieve Vehicle with Fleetio

Retrieves a specific vehicle from Fleetio.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/:id`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Retrieve Vehicle](https://developer.fleetio.com/docs/api/vehicles-show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Fleetio ID of the relevant Vehicle.  You may also look up Vehicles by their VIN, license plate, or other external ID. See the guide on [External Vehicle Ids](/docs/guides/vehicles/external-vehicle-ids) for information on how to set this up. |
