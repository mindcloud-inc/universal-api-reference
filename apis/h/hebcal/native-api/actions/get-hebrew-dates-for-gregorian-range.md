# Get Hebrew Dates for Gregorian Range with Hebcal

Retrieves Hebrew dates for a Gregorian date range in Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/converter`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Hebrew Dates for Gregorian Range](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | Gregorian start date in YYYY-MM-DD format. |
| `end` | query | `string` | yes | Gregorian end date in YYYY-MM-DD format. |
