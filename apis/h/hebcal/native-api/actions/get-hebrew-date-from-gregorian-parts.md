# Get Hebrew Date from Gregorian Parts with Hebcal

Retrieves a Hebrew date from Gregorian date parts in Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/converter`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Hebrew Date from Gregorian Parts](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gy` | query | `string` | yes | Gregorian year. |
| `gm` | query | `string` | yes | Gregorian month number. |
| `gd` | query | `string` | yes | Gregorian day of month. |
| `strict` | query | `string` | no | Return an error for invalid dates when enabled. |
