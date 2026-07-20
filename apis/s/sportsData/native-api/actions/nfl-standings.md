# NFL Standings with SportsData

Retrieves NFL standings from SportsData.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/nfl/scores/json/Standings/:season`
- **Base URL:** `https://api.sportsdata.io`
- **Official documentation:** [NFL Standings](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `season` | path | `string` | yes | NFL season year for standings. |
