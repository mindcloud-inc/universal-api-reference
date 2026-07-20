# List Climate Data with NCEI Climate Data

Finds climate data in NCEI Climate Data by dataset and date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/data`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [List Climate Data](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetid` | query | `string` | yes | Required single dataset identifier, for example GHCND. |
| `datatypeid` | query | `string` | no | Optional data type id such as TAVG, TMIN, TMAX, or PRCP. |
| `includemetadata` | query | `boolean` | no | Set false to skip result metadata for faster responses. |
| `locationid` | query | `string` | no | Optional location id such as ZIP:28801 or FIPS:37. |
| `sortfield` | query | `string` | no | Optional sort field documented by CDO. |
| `sortorder` | query | `string` | no | Sort direction: asc or desc. |
| `stationid` | query | `string` | no | Optional station id such as COOP:010008 or GHCND:USC00010008. |
| `units` | query | `list` | no | Optional units value: metric or standard. Accepted values: `0`, `1`. |
| `startdate` | query | `string` | yes | Required start date in YYYY-MM-DD format. Use a date string, not a date-time. |
| `enddate` | query | `string` | yes | Required end date in YYYY-MM-DD format. Use a date string, not a date-time. |
