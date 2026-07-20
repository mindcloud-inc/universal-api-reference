# List Game Havoc Stats with College Football Data

Retrieves game havoc statistics from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/stats/game/havoc`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Game Havoc Stats](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if team not specified |
| `team` | query | `string` | no | Team filter, required if year not specified |
| `week` | query | `number` | no | Optional week filter |
| `opponent` | query | `string` | no | Optional opponent filter |
| `seasonType` | query | `string` | no | Optional season type filter |
