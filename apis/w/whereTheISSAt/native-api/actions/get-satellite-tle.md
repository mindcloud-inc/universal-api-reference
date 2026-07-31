# Get Satellite TLE with Where the ISS at

## Endpoint

- **Method:** `GET`
- **Path:** `/satellites/:satelliteId/tles`
- **Base URL:** `https://api.wheretheiss.at/v1`
- **Official documentation:** [Get Satellite TLE](https://wheretheiss.at/w/developer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `satelliteId` | path | `number` | yes | NORAD catalog ID; use 25544 for the International Space Station. |
