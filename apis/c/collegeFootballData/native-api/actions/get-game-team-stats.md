# List Game Team Stats with College Football Data

Retrieves team box score statistics from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/games/teams`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Game Team Stats](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Required year filter (along with one of week, team, or conference), unless id is specified |
| `week` | query | `number` | no | Optional week filter, required if team and conference not specified |
| `team` | query | `string` | no | Optional team filter, required if week and conference not specified |
| `conference` | query | `string` | no | Optional conference filter, required if week and team not specified |
| `classification` | query | `string` | no | Optional division classification filter |
| `seasonType` | query | `string` | no | Optional season type filter |
| `id` | query | `number` | no | Optional id filter to retrieve a single game |
