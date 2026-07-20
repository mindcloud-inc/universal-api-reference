# Search Map Locations By Address with NiftyImages

Finds map locations in NiftyImages by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/Maps/GetLocations`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Search Map Locations By Address](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages map URL. |
| `address` | query | `string` | yes | Address to search for. |
