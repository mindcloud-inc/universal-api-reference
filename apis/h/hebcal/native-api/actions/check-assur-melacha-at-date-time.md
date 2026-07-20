# Check Assur Melacha at Date Time with Hebcal

Checks whether work is forbidden at a date and time in Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/zmanim`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Check Assur Melacha at Date Time](https://www.hebcal.com/home/4984/assur-melacha-work-forbidden-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dt` | query | `string` | yes | ISO 8601 date-time to check. |
| `geonameid` | query | `string` | no | GeoNames numeric ID for the location. |
| `zip` | query | `string` | no | United States ZIP code for the location. |
| `latitude` | query | `string` | no | Latitude for the location. |
| `longitude` | query | `string` | no | Longitude for the location. |
