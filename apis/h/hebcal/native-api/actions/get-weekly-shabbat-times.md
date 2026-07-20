# Get Weekly Shabbat Times with Hebcal

Retrieves weekly Shabbat times from Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/shabbat`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Weekly Shabbat Times](https://www.hebcal.com/home/197/shabbat-times-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lg` | query | `string` | no | Event title language. |
| `b` | query | `string` | no | Minutes before sunset for candle lighting. |
| `m` | query | `string` | no | Fixed minutes after sundown for havdalah. |
| `geonameid` | query | `string` | no | GeoNames numeric ID for the location. |
| `zip` | query | `string` | no | United States ZIP code for the location. |
| `latitude` | query | `string` | no | Latitude for the location. |
| `longitude` | query | `string` | no | Longitude for the location. |
