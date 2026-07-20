# Search Map Locations By Nifty ID with NiftyImages

Finds map locations in NiftyImages by Nifty ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/Maps/GetLocations`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Search Map Locations By Nifty ID](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages map URL. |
| `niftyID` | query | `string` | yes | NiftyImages-assigned location ID. |
