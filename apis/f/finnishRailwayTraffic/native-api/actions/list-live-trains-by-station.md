# List live trains by station with Finnish Railway Traffic

Retrieves live trains for a station from Finnish Railway Traffic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/live-trains/station/:station`
- **Base URL:** `https://rata.digitraffic.fi`
- **Official documentation:** [List live trains by station](https://rata.digitraffic.fi/swagger/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `station` | path | `string` | yes | Station short code, for example HKI for Helsinki Central. |
