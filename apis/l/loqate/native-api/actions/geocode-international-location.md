# Geocode International Location with Loqate

Geocodes an international location with Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/Geocoding/International/Geocode/v1.10/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Geocode International Location](https://docs.loqate.com/api-reference/geocode/geocoding/international-geocode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Country` | query | `string` | yes | The country to search in. |
| `Location` | query | `string` | yes | The location to geocode. |
