# List Monitoring Site Observations with AirNow

Retrieves monitoring site observations from AirNow within a geographic area.

## Endpoint

- **Method:** `GET`
- **Path:** `/aq/data/`
- **Base URL:** `https://www.airnowapi.org`
- **Official documentation:** [List Monitoring Site Observations](https://docs.airnowapi.org/ObservationsByMonitoringSite/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | Start date/time in AirNow format, for example 2026-04-08T00. |
| `endDate` | query | `string` | yes | End date/time in AirNow format, for example 2026-04-08T01. |
| `parameters` | query | `string` | yes | Comma-separated pollutant parameters, such as OZONE,PM25. |
| `BBOX` | query | `string` | yes | Bounding box in west,south,east,north order. |
| `dataType` | query | `string` | yes | A for AQI, B for concentrations, or C for both. |
| `verbose` | query | `string` | no | Set to 1 to include agency and site metadata. |
| `monitorType` | query | `string` | no | Monitor type filter. |
| `includerawconcentrations` | query | `string` | no | Set to 1 to include raw concentration values when supported. |
