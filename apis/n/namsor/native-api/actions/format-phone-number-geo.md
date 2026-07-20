# Format Phone Number Geo with Namsor

Retrieves verified phone number details in Namsor by country.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/phoneCodeGeo/:firstName/:lastName/:phoneNumber/:countryIso2`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Format Phone Number Geo](https://namsor.app/api-documentation/phone-number-format/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryIso2` | path | `string` | yes | Two-letter ISO country code. |
| `firstName` | path | `string` | yes | First name. |
| `lastName` | path | `string` | yes | Last name. |
| `phoneNumber` | path | `string` | yes | Phone number. |
