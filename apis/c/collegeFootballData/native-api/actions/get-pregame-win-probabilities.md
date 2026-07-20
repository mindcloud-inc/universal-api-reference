# List Pregame Win Probabilities with College Football Data

Retrieves pregame win probabilities from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/metrics/wp/pregame`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Pregame Win Probabilities](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Optional year filter |
| `week` | query | `number` | no | Optional week filter |
| `seasonType` | query | `string` | no | Optional season type filter |
| `team` | query | `string` | no | Optional team filter |
