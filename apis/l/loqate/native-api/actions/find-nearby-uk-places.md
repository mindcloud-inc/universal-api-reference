# Find Nearby UK Places with Loqate

Finds nearby UK places with Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/Geocoding/UK/RetrieveNearestPlaces/v1.20/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Find Nearby UK Places](https://docs.loqate.com/api-reference/geocode/geocoding/uk-retrievenearestplaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CentrePoint` | query | `string` | yes | The centre point for the UK search. |
| `MaximumItems` | query | `number` | no | Maximum number of places to return. |
| `MaximumRadius` | query | `number` | no | Maximum radius in KM for the search. |
