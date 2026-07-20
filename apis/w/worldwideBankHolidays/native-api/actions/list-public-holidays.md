# List Public Holidays with Worldwide Bank Holidays

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/PublicHolidays/{{year}}/{{countryCode}}`
- **Base URL:** `https://date.nager.at`
- **Official documentation:** [List Public Holidays](https://date.nager.at/API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `number` | yes | Calendar year for holiday lookup. |
| `countryCode` | path | `string` | yes | ISO 3166-1 alpha-2 country code, such as US or DE. |
