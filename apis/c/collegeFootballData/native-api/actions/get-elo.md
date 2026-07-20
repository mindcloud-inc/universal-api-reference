# List Elo with College Football Data

Retrieves historical Elo ratings from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ratings/elo`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Elo](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Optional year filter |
| `week` | query | `number` | no | Optional week filter, defaults to last available week in the season |
| `seasonType` | query | `string` | no | Optional season type filter |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference filter |
