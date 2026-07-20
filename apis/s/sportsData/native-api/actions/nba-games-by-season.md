# NBA Games By Season with SportsData

Retrieves NBA games from SportsData by season.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/nba/scores/json/Games/:season`
- **Base URL:** `https://api.sportsdata.io`
- **Official documentation:** [NBA Games By Season](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `season` | path | `string` | yes | NBA season year for the games feed. |
