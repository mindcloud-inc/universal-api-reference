# List Team Stats with College Football Data

Retrieves team season statistics from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/stats/season`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Team Stats](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if team not specified |
| `team` | query | `string` | no | Team filter, required if year not specified |
| `conference` | query | `string` | no | Optional conference filter |
| `startWeek` | query | `number` | no | Optional week start range filter |
| `endWeek` | query | `number` | no | Optional week end range filter |
