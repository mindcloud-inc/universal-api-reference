# List Adjusted Player Rushing Stats with College Football Data

Retrieves opponent-adjusted player rushing statistics from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/wepa/players/rushing`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Adjusted Player Rushing Stats](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Optional year filter |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference abbreviation filter |
| `position` | query | `string` | no | Optional position abbreviation filter |
