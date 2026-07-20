# Update Location with BoxHero

Updates an existing location in BoxHero.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/locations/:location_id`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Update Location](https://rest.boxhero-app.com/docs/api#/locations/LocationsController_updateLocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_id` | path | `number` | yes | Unique identifier for the location |
| `memo` | body | `string` | no | Notes related to the location |
| `name` | body | `string` | no | The name of the location |
