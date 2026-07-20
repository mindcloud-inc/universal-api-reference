# List Upcoming Public Holidays with Worldwide Bank Holidays

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/NextPublicHolidays/{{countryCode}}`
- **Base URL:** `https://date.nager.at`
- **Official documentation:** [List Upcoming Public Holidays](https://date.nager.at/openapi/v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryCode` | path | `string` | yes | ISO 3166-1 alpha-2 country code, such as US or DE. |
