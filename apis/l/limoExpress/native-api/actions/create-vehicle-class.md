# Create Vehicle Class with LimoExpress

Creates a new vehicle class in LimoExpress.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/integration/vehicle-classes`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [Create Vehicle Class](https://api.limoexpress.me/api/docs/v1#/Vehicle%20Classes/createAOrganisationVehicleClass)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the vehicle class |
| `active` | body | `boolean` | yes | Active flag for vehicle class |
| `available_for_public` | body | `boolean` | yes | Whether class is available on public booking page |
