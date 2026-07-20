# List Media with College Football Data

Retrieves game media information from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/games/media`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Media](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `seasonType` | query | `string` | no | Optional season type filter |
| `week` | query | `number` | no | Optional week filter |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference filter |
| `mediaType` | query | `string` | no | Optional media type filter |
| `classification` | query | `string` | no | Optional division classification filter |
