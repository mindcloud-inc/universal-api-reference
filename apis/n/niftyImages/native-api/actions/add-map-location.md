# Add Map Location with NiftyImages

Creates a new map location in NiftyImages.

## Endpoint

- **Method:** `POST`
- **Path:** `/Maps/AddLocation`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Add Map Location](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages map URL. |
| `Address` | body | `string` | yes | Address of the new location. |
| `LocationID` | body | `string` | no | Optional location ID for the location. |
| `Properties[]` | body | `array<object>` | no | Optional properties to attach to the location. |
| `Properties[].Name` | body | `string` | no | Property name. |
| `Properties[].Value` | body | `string` | no | Property value. |
