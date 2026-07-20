# List Games with College Football Data

Retrieves historical games from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/games`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Games](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Required year filter (except when id is specified) |
| `week` | query | `number` | no | Optional week filter |
| `seasonType` | query | `string` | no | Optional season type filter |
| `classification` | query | `string` | no | Optional division classification filter |
| `team` | query | `string` | no | Optional team filter |
| `home` | query | `string` | no | Optional home team filter |
| `away` | query | `string` | no | Optional away team filter |
| `conference` | query | `string` | no | Optional conference filter |
| `id` | query | `number` | no | Game id filter to retrieve a single game |
