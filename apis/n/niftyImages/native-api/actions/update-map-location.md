# Update Map Location with NiftyImages

Updates an existing map location in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Maps/UpdateLocation`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Map Location](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages map URL. |
| `NiftyID` | body | `string` | no | NiftyImages location ID to update. |
| `Address` | body | `string` | no | New address for the location. |
| `Latitude` | body | `number` | no | New latitude for the location. |
| `Longitude` | body | `number` | no | New longitude for the location. |
| `LocationID` | body | `string` | no | Location ID for the location. |
| `Properties[]` | body | `array<object>` | no | Optional properties to attach to the location. |
| `Properties[].Name` | body | `string` | no | Property name. |
| `Properties[].Value` | body | `string` | no | Property value. |
