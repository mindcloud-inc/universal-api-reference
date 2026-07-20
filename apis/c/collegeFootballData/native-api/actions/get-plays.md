# List Plays with College Football Data

Retrieves historical plays from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/plays`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Plays](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `week` | query | `number` | yes | Required week filter |
| `team` | query | `string` | no | Optional team filter |
| `offense` | query | `string` | no | Optional offensive team filter |
| `defense` | query | `string` | no | Optional defensive team filter |
| `offenseConference` | query | `string` | no | Optional offensive conference filter |
| `defenseConference` | query | `string` | no | Optional defensive conference filter |
| `conference` | query | `string` | no | Optional conference filter |
| `playType` | query | `string` | no | Optoinal play type abbreviation filter |
| `seasonType` | query | `string` | no | Optional season type filter |
| `classification` | query | `string` | no | Optional division classification filter |
