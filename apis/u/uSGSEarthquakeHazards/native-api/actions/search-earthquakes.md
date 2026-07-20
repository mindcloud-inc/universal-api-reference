# Search Earthquakes with USGS Earthquake Hazards

Finds earthquakes in USGS Earthquake Hazards by search parameters.

## Endpoint

- **Method:** `GET`
- **Path:** `/fdsnws/event/1/query`
- **Base URL:** `https://earthquake.usgs.gov`
- **Official documentation:** [Search Earthquakes](https://earthquake.usgs.gov/fdsnws/event/1/)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starttime` | query | `string` | no | Only return events on or after this ISO8601 UTC time. |
| `endtime` | query | `string` | no | Only return events on or before this ISO8601 UTC time. |
| `minmagnitude` | query | `number` | no | Only return events with magnitude greater than or equal to this value. |
| `maxmagnitude` | query | `number` | no | Only return events with magnitude less than or equal to this value. |
| `latitude` | query | `number` | no | Latitude for radius search. Use with longitude and maximum radius in kilometers. |
| `longitude` | query | `number` | no | Longitude for radius search. Use with latitude and maximum radius in kilometers. |
| `maxradiuskm` | query | `number` | no | Maximum distance in kilometers from the latitude and longitude point. |
| `eventtype` | query | `string` | no | Limit results to a USGS event type such as earthquake. |
| `orderby` | query | `string` | no | USGS event ordering mode. Accepted values: `0`, `1`, `2`, `3`. |
| `limit` | query | `number` | no | Maximum number of events to return. |
| `offset` | query | `number` | no | One-based result offset for USGS catalog pagination. |
