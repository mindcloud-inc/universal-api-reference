# List Predicted Points Added By Player Season with College Football Data

Retrieves player PPA statistics by season from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ppa/players/season`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Predicted Points Added By Player Season](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if playerId not specified |
| `conference` | query | `string` | no | Optional conference abbreviation filter |
| `team` | query | `string` | no | Optional team filter |
| `position` | query | `string` | no | Optional position abbreviation filter |
| `playerId` | query | `string` | no | Player ID filter, required if year not specified |
| `threshold` | query | `number` | no | Threshold value for minimum number of plays |
| `excludeGarbageTime` | query | `boolean` | no | Optional flag to exclude garbage time plays |
