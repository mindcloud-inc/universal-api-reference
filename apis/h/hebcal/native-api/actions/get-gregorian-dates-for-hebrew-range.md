# Get Gregorian Dates for Hebrew Range with Hebcal

Retrieves Gregorian dates for a Hebrew date range in Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/converter`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Gregorian Dates for Hebrew Range](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hy` | query | `string` | yes | Hebrew year. |
| `hm` | query | `string` | yes | Hebrew month name. |
| `hd` | query | `string` | yes | Hebrew day of month. |
| `ndays` | query | `string` | yes | Number of days to calculate. |
| `strict` | query | `string` | no | Return an error for invalid dates when enabled. |
