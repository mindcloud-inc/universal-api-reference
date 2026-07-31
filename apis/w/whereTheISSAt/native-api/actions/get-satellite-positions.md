# Get Satellite Positions with Where the ISS at

## Endpoint

- **Method:** `GET`
- **Path:** `/satellites/:satelliteId/positions`
- **Base URL:** `https://api.wheretheiss.at/v1`
- **Official documentation:** [Get Satellite Positions](https://wheretheiss.at/w/developer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `satelliteId` | path | `number` | yes | NORAD catalog ID; use 25544 for the International Space Station. |
| `timestamps` | query | `string` | yes | Required comma-delimited Unix timestamps, up to 10 values. |
| `units` | query | `string` | no | Optional distance and velocity units: miles or kilometers; provider defaults to kilometers. |
