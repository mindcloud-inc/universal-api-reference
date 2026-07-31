# Get Satellite Position with Where the ISS at

## Endpoint

- **Method:** `GET`
- **Path:** `/satellites/:satelliteId`
- **Base URL:** `https://api.wheretheiss.at/v1`
- **Official documentation:** [Get Satellite Position](https://wheretheiss.at/w/developer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `satelliteId` | path | `number` | yes | NORAD catalog ID; use 25544 for the International Space Station. |
| `units` | query | `string` | no | Optional distance and velocity units: miles or kilometers; provider defaults to kilometers. |
| `timestamp` | query | `number` | no | Optional Unix timestamp for the orbital position; provider defaults to the current timestamp. |
