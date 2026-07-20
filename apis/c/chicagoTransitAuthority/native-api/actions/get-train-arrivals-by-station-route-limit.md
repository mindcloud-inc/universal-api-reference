# Get Train Arrivals by Station Route Limit with Chicago Transit Authority

Retrieves limited train arrival predictions in Chicago Transit Authority by station and route.

## Endpoint

- **Method:** `GET`
- **Path:** `/ttarrivals.aspx`
- **Base URL:** `https://lapi.transitchicago.com/api/1.0`
- **Official documentation:** [Get Train Arrivals by Station Route Limit](https://www.transitchicago.com/developers/ttdocs/default.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapid` | query | `string` | yes | CTA station map ID, such as 40380 for Clark/Lake. |
| `rt` | query | `list` | yes | CTA rail route code. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `max` | query | `number` | yes | Maximum number of arrivals to return. |
