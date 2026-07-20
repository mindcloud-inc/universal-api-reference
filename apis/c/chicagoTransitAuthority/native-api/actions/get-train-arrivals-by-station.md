# Get Train Arrivals by Station with Chicago Transit Authority

Retrieves train arrival predictions in Chicago Transit Authority by station.

## Endpoint

- **Method:** `GET`
- **Path:** `/ttarrivals.aspx`
- **Base URL:** `https://lapi.transitchicago.com/api/1.0`
- **Official documentation:** [Get Train Arrivals by Station](https://www.transitchicago.com/developers/ttdocs/default.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapid` | query | `string` | yes | CTA station map ID from the Train Tracker docs, such as 40380 for Clark/Lake. |
| `rt` | query | `list` | no | Optional CTA rail route code such as Red, Blue, Brn, Org, Pnk, G, or Y. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `max` | query | `number` | no | Optional maximum number of arrivals to return. |
