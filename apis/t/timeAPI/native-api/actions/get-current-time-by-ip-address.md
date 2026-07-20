# Get Current Time By IP Address with TimeAPI

Retrieves the current time by IP address from TimeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/time/current/ip`
- **Base URL:** `https://www.timeapi.io`
- **Official documentation:** [Get Current Time By IP Address](https://www.timeapi.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddress` | query | `string` | yes | IPv4 address, for example 8.8.8.8. |
