# Find Nearby International Places with Loqate

Finds nearby international places with Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/Geocoding/International/RetrieveNearestPlaces/v1.00/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Find Nearby International Places](https://docs.loqate.com/api-reference/geocode/geocoding/international-retrievenearestplaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CentrePoint` | query | `string` | yes | The centre point for the search. |
| `Country` | query | `string` | no | Optional ISO3 country code for place-name searches. |
| `MaximumItems` | query | `number` | no | Maximum number of places to return. |
| `MaximumRadius` | query | `number` | no | Maximum radius in KM for the search. |
