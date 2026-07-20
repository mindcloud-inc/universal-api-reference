# Delete Map Location By Nifty ID with NiftyImages

Deletes a map location from NiftyImages by Nifty ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/Maps/DeleteLocation`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Delete Map Location By Nifty ID](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages map URL. |
| `niftyID` | query | `string` | yes | NiftyImages location ID to delete. |
