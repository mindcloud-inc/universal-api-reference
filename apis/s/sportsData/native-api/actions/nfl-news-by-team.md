# NFL News By Team with SportsData

Retrieves NFL news from SportsData by team.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/nfl/scores/json/NewsByTeam/:team`
- **Base URL:** `https://api.sportsdata.io`
- **Official documentation:** [NFL News By Team](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | NFL team key used by SportsData news endpoints. |
