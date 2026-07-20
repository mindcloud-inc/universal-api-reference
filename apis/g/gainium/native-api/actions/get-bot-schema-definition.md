# Get Bot Schema Definition with Gainium

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/discovery/bots/:botType`
- **Base URL:** `https://api.gainium.io`
- **Official documentation:** [Get Bot Schema Definition](https://api.gainium.io/api/docs/v2#/Discovery/getDiscoveryBot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botType` | path | `list` | yes | Bot type. Accepted values: `0`, `1`, `2`. |
| `section` | query | `string` | no | Return only one schema section. |
