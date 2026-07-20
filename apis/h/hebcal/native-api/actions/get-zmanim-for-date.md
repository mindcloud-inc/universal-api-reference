# Get Zmanim for Date with Hebcal

Retrieves zmanim for a date from Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/zmanim`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Zmanim for Date](https://www.hebcal.com/home/1663/zmanim-halachic-times-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Gregorian date in YYYY-MM-DD format. |
| `geonameid` | query | `string` | no | GeoNames numeric ID for the location. |
| `zip` | query | `string` | no | United States ZIP code for the location. |
| `latitude` | query | `string` | no | Latitude for the location. |
| `longitude` | query | `string` | no | Longitude for the location. |
