# List Drives with College Football Data

Retrieves historical drives from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/drives`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Drives](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `seasonType` | query | `string` | no | Optional season type filter |
| `week` | query | `number` | no | Optional week filter |
| `team` | query | `string` | no | Optional team filter |
| `offense` | query | `string` | no | Optional offensive team filter |
| `defense` | query | `string` | no | Optional defensive team filter |
| `conference` | query | `string` | no | Optional conference filter |
| `offenseConference` | query | `string` | no | Optional offensive team conference filter |
| `defenseConference` | query | `string` | no | Optional defensive team conference filter |
| `classification` | query | `string` | no | Optional division classification filter |
