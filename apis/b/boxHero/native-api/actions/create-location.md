# Create Location with BoxHero

Creates a new location in BoxHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/locations`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Create Location](https://rest.boxhero-app.com/docs/api#/locations/LocationsController_createLocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memo` | body | `string` | no | Notes related to the location |
| `name` | body | `string` | yes | The name of the location |
