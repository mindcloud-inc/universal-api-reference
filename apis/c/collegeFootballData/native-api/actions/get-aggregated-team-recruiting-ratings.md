# List Aggregated Team Recruiting Ratings with College Football Data

Retrieves aggregated team recruiting ratings from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/recruiting/groups`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Aggregated Team Recruiting Ratings](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference filter |
| `recruitType` | query | `string` | no | Optional recruit type filter, defaults to HighSchool |
| `startYear` | query | `number` | no | Optional start year range, defaults to 2000 |
| `endYear` | query | `number` | no | Optional end year range, defaults to current year |
