# Update Vehicle Class with LimoExpress

Updates an existing vehicle class in LimoExpress.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/vehicle-classes`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [Update Vehicle Class](https://api.limoexpress.me/api/docs/v1#/Vehicle%20Classes/updateAOrganisationVehicleClass)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Vehicle class identifier |
| `name` | body | `string` | yes | Name of the vehicle class |
| `active` | body | `boolean` | yes | Active flag for vehicle class |
| `available_for_public` | body | `boolean` | yes | Whether class is available on public booking page |
