# List Torah Reading Calendar Events with Hebcal

Retrieves Torah reading calendar events from Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/hebcal`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [List Torah Reading Calendar Events](https://www.hebcal.com/home/195/jewish-calendar-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `string` | no | Gregorian year or now. |
| `month` | query | `string` | no | Gregorian month number or x for whole year. |
| `start` | query | `string` | no | Gregorian start date in YYYY-MM-DD format. |
| `end` | query | `string` | no | Gregorian end date in YYYY-MM-DD format. |
| `lg` | query | `string` | no | Event title language. |
| `i` | query | `string` | no | Use Israel Torah reading schedule when enabled. |
| `geonameid` | query | `string` | no | GeoNames numeric ID for the location. |
| `zip` | query | `string` | no | United States ZIP code for the location. |
| `latitude` | query | `string` | no | Latitude for the location. |
| `longitude` | query | `string` | no | Longitude for the location. |
