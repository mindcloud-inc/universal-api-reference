# Search live trains between stations with Finnish Railway Traffic

Finds live trains between stations in Finnish Railway Traffic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/live-trains/station/:departure_station/:arrival_station`
- **Base URL:** `https://rata.digitraffic.fi`
- **Official documentation:** [Search live trains between stations](https://rata.digitraffic.fi/swagger/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departure_station` | path | `string` | yes | Departure station short code, for example HKI. |
| `arrival_station` | path | `string` | yes | Arrival station short code, for example TPE. |
