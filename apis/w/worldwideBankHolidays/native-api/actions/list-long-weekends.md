# List Long Weekends with Worldwide Bank Holidays

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/LongWeekend/{{year}}/{{countryCode}}`
- **Base URL:** `https://date.nager.at`
- **Official documentation:** [List Long Weekends](https://date.nager.at/openapi/v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `number` | yes | Calendar year for long weekend lookup. |
| `countryCode` | path | `string` | yes | ISO 3166-1 alpha-2 country code, such as US or DE. |
| `availableBridgeDays` | query | `number` | no | Optional number of available bridge days, from 1 to 100. |
| `subdivisionCode` | query | `string` | no | Optional ISO 3166-2 subdivision code. |
