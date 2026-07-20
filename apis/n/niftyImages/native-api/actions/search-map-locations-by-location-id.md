# Search Map Locations By Location ID with NiftyImages

Finds map locations in NiftyImages by location ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/Maps/GetLocations`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Search Map Locations By Location ID](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages map URL. |
| `locationID` | query | `string` | yes | Location ID from your import. |
