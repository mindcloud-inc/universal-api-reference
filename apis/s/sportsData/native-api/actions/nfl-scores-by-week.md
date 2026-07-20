# NFL Scores By Week with SportsData

Retrieves NFL scores from SportsData by week.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/nfl/scores/json/ScoresByWeek/:season/:week`
- **Base URL:** `https://api.sportsdata.io`
- **Official documentation:** [NFL Scores By Week](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `season` | path | `string` | yes | NFL season code for the scores feed, for example 2025REG. |
| `week` | path | `string` | yes | NFL week number within the selected season code. |
