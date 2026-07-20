# NBA Games By Date with SportsData

Retrieves NBA games from SportsData by date.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/nba/scores/json/GamesByDate/:date`
- **Base URL:** `https://api.sportsdata.io`
- **Official documentation:** [NBA Games By Date](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Game date for the NBA games feed. |
