# Get Indicator Definition with Gainium

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/discovery/indicators/:type`
- **Base URL:** `https://api.gainium.io`
- **Official documentation:** [Get Indicator Definition](https://api.gainium.io/api/docs/v2#/Discovery/getDiscoveryIndicator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | no | Filter indicator intervals to one exchange. |
| `type` | path | `string` | yes | Indicator type. |
