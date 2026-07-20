# Name Diaspora with Namsor

Retrieves the likely diaspora for a name in Namsor by country.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/diaspora/:countryIso2/:firstName/:lastName`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Name Diaspora](https://namsor.app/api-documentation/ethnicity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryIso2` | path | `string` | yes | Two-letter ISO country code. |
| `firstName` | path | `string` | yes | First name. |
| `lastName` | path | `string` | yes | Last name. |
