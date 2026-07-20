# List Datasets with NCEI Climate Data

Finds climate datasets in NCEI Climate Data by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasets`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [List Datasets](https://www.ncei.noaa.gov/cdo-web/webservices/v2#datasets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datatypeid` | query | `string` | no | Filter datasets by data type id, such as TAVG or TOBS. |
| `enddate` | query | `string` | no | Filter datasets that have data before this YYYY-MM-DD date. |
| `locationid` | query | `string` | no | Filter datasets by location id, such as FIPS:37 or ZIP:28801. |
| `sortfield` | query | `string` | no | Sort by id, name, mindate, maxdate, or datacoverage. |
| `sortorder` | query | `string` | no | Sort direction: asc or desc. |
| `startdate` | query | `string` | no | Filter datasets that have data after this YYYY-MM-DD date. |
| `stationid` | query | `string` | no | Filter datasets by station id, such as COOP:010957. |
