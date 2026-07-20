# Get Matchup with College Football Data

Retrieves historical team matchup details from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/matchup`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [Get Matchup](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team1` | query | `string` | yes | First team to compare |
| `team2` | query | `string` | yes | Second team to compare |
| `minYear` | query | `number` | no | Optional starting year |
| `maxYear` | query | `number` | no | Optional ending year |
