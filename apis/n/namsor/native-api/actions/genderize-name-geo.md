# Genderize Name Geo with Namsor

Retrieves the likely gender for a name in Namsor by country.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/genderGeo/:firstName/:lastName/:countryIso2`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Genderize Name Geo](https://namsor.app/api-documentation/gender-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryIso2` | path | `string` | yes | Two-letter ISO country code. |
| `firstName` | path | `string` | yes | First name. |
| `lastName` | path | `string` | yes | Last name. |
