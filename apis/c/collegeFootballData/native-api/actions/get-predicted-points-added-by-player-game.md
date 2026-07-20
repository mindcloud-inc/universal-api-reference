# List Predicted Points Added By Player Game with College Football Data

Retrieves player PPA statistics by game from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ppa/players/games`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Predicted Points Added By Player Game](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `week` | query | `number` | no | Week filter, required if team not specified |
| `seasonType` | query | `string` | no | Optional season type filter |
| `team` | query | `string` | no | Team filter, required if week not specified |
| `position` | query | `string` | no | Optional player position abbreviation filter |
| `playerId` | query | `string` | no | Optional player ID filter |
| `threshold` | query | `number` | no | Threshold value for minimum number of plays |
| `excludeGarbageTime` | query | `boolean` | no | Optional flag to exclude garbage time plays |
