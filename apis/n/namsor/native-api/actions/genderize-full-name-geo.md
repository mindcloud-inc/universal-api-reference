# Genderize Full Name Geo with Namsor

Retrieves the likely gender for a full name in Namsor by country.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/genderFullGeo/:fullName/:countryIso2`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Genderize Full Name Geo](https://namsor.app/api-documentation/gender-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryIso2` | path | `string` | yes | Two-letter ISO country code. |
| `fullName` | path | `string` | yes | Full personal name. |
