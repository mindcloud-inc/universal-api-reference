# Delete Map Location By Location ID with NiftyImages

Deletes a map location from NiftyImages by location ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/Maps/DeleteLocation`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Delete Map Location By Location ID](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages map URL. |
| `locationID` | query | `string` | yes | Location ID to delete. |
