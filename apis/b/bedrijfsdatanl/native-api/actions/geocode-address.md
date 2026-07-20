# Geocode Address with Bedrijfsdata.nl

## Endpoint

- **Method:** `GET`
- **Path:** `/geocoding`
- **Base URL:** `https://fapi.bedrijfsdata.nl/v1.2`
- **Official documentation:** [Geocode Address](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | ISO2 country code. |
| `q` | query | `string` | no | Address or place query to geocode. |
