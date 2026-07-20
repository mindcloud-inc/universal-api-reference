# List Predicted Points Added By Game with College Football Data

Retrieves team PPA metrics by game from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ppa/games`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Predicted Points Added By Game](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `week` | query | `number` | no | Optional week filter |
| `seasonType` | query | `string` | no | Optional season type filter |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference abbreviation filter |
| `excludeGarbageTime` | query | `boolean` | no | Optional flag to exclude garbage time plays |
