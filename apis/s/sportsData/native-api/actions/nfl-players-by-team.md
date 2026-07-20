# NFL Players By Team with SportsData

Retrieves NFL player details from SportsData by team.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/nfl/scores/json/Players/:team`
- **Base URL:** `https://api.sportsdata.io`
- **Official documentation:** [NFL Players By Team](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | NFL team abbreviation. |
