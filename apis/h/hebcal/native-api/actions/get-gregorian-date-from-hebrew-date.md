# Get Gregorian Date from Hebrew Date with Hebcal

Retrieves a Gregorian date from a Hebrew date in Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/converter`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Gregorian Date from Hebrew Date](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hy` | query | `string` | yes | Hebrew year. |
| `hm` | query | `string` | yes | Hebrew month name. |
| `hd` | query | `string` | yes | Hebrew day of month. |
| `strict` | query | `string` | no | Return an error for invalid dates when enabled. |
