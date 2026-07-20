# Count Earthquakes with USGS Earthquake Hazards

Counts earthquakes matching a USGS Earthquake Hazards query.

## Endpoint

- **Method:** `GET`
- **Path:** `/fdsnws/event/1/count`
- **Base URL:** `https://earthquake.usgs.gov`
- **Official documentation:** [Count Earthquakes](https://earthquake.usgs.gov/fdsnws/event/1/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starttime` | query | `string` | no | Only count events on or after this ISO8601 UTC time. |
| `endtime` | query | `string` | no | Only count events on or before this ISO8601 UTC time. |
| `minmagnitude` | query | `number` | no | Only count events with magnitude greater than or equal to this value. |
