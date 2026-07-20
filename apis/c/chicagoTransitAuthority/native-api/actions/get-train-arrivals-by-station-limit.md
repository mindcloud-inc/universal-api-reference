# Get Train Arrivals by Station Limit with Chicago Transit Authority

Retrieves limited train arrival predictions in Chicago Transit Authority by station.

## Endpoint

- **Method:** `GET`
- **Path:** `/ttarrivals.aspx`
- **Base URL:** `https://lapi.transitchicago.com/api/1.0`
- **Official documentation:** [Get Train Arrivals by Station Limit](https://www.transitchicago.com/developers/ttdocs/default.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapid` | query | `string` | yes | CTA station map ID, such as 40380 for Clark/Lake. |
| `max` | query | `number` | yes | Maximum number of arrivals to return. |
