# List Lines with College Football Data

Retrieves historical betting lines from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/lines`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Lines](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gameId` | query | `number` | no | Optional gameId filter |
| `year` | query | `number` | no | Year filter, required if game id not specified |
| `seasonType` | query | `string` | no | Optional season type filter |
| `week` | query | `number` | no | Optional week filter |
| `team` | query | `string` | no | Optional team filter |
| `home` | query | `string` | no | Optional home team filter |
| `away` | query | `string` | no | Optional away team filter |
| `conference` | query | `string` | no | Optional conference filter |
| `provider` | query | `string` | no | Optional provider name filter |
