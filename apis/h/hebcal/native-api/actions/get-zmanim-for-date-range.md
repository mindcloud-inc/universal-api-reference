# Get Zmanim for Date Range with Hebcal

Retrieves zmanim for a date range from Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/zmanim`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Zmanim for Date Range](https://www.hebcal.com/home/1663/zmanim-halachic-times-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | Gregorian start date in YYYY-MM-DD format. |
| `end` | query | `string` | yes | Gregorian end date in YYYY-MM-DD format. |
| `geonameid` | query | `string` | no | GeoNames numeric ID for the location. |
| `zip` | query | `string` | no | United States ZIP code for the location. |
| `latitude` | query | `string` | no | Latitude for the location. |
| `longitude` | query | `string` | no | Longitude for the location. |
