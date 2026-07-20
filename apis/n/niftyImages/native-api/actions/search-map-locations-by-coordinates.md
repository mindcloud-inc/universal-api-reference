# Search Map Locations By Coordinates with NiftyImages

Finds map locations in NiftyImages by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/Maps/GetLocations`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Search Map Locations By Coordinates](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages map URL. |
| `lat` | query | `number` | yes | Latitude to search around. |
| `lng` | query | `number` | yes | Longitude to search around. |
