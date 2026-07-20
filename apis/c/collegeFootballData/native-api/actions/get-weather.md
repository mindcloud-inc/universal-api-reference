# List Weather with College Football Data

Retrieves game weather data from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/games/weather`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Weather](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if game id not specified |
| `seasonType` | query | `string` | no | Optional season type filter |
| `week` | query | `number` | no | Optional week filter |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference filter |
| `classification` | query | `string` | no | Optional division classification filter |
| `gameId` | query | `number` | no | Filter for retrieving a single game |
