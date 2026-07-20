# List Daf Yomi Readings with Hebcal

Retrieves Daf Yomi readings from Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/hebcal`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [List Daf Yomi Readings](https://www.hebcal.com/home/195/jewish-calendar-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | no | Gregorian start date in YYYY-MM-DD format. |
| `end` | query | `string` | no | Gregorian end date in YYYY-MM-DD format. |
