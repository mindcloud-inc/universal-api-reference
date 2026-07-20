# NFL Schedules By Season with SportsData

Retrieves NFL schedules from SportsData by season.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/nfl/scores/json/Schedules/:season`
- **Base URL:** `https://api.sportsdata.io`
- **Official documentation:** [NFL Schedules By Season](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `season` | path | `string` | yes | NFL season year for the schedule feed. |
