# Get Hebrew Date from Gregorian Date with Hebcal

Retrieves a Hebrew date from a Gregorian date in Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/converter`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Hebrew Date from Gregorian Date](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Gregorian date in YYYY-MM-DD format. |
| `strict` | query | `string` | no | Return an error for invalid dates when enabled. |
