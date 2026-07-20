# List Player Season Stats with College Football Data

Retrieves player season statistics from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/stats/player/season`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Player Season Stats](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `conference` | query | `string` | no | Optional conference filter |
| `team` | query | `string` | no | Optional team filter |
| `startWeek` | query | `number` | no | Optional starting week range |
| `endWeek` | query | `number` | no | Optional ending week range |
| `seasonType` | query | `string` | no | Optional season type filter |
| `category` | query | `string` | no | Optional category filter |
