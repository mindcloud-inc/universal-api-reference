# NBA Standings with SportsData

Retrieves NBA standings from SportsData.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/nba/scores/json/Standings/:season`
- **Base URL:** `https://api.sportsdata.io`
- **Official documentation:** [NBA Standings](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `season` | path | `string` | yes | NBA season year for standings. |
