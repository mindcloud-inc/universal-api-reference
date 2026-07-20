# Check Today Public Holiday with Worldwide Bank Holidays

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/IsTodayPublicHoliday/{{countryCode}}`
- **Base URL:** `https://date.nager.at`
- **Official documentation:** [Check Today Public Holiday](https://date.nager.at/openapi/v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryCode` | path | `string` | yes | ISO 3166-1 alpha-2 country code, such as US or DE. |
| `countyCode` | query | `string` | no | Optional subdivision/county code. |
| `offset` | query | `number` | no | Optional UTC timezone offset from -12 to 12. |
