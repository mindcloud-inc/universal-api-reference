# List Adjusted Player Passing Stats with College Football Data

Retrieves opponent-adjusted player passing statistics from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/wepa/players/passing`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Adjusted Player Passing Stats](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Optional year filter |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference abbreviation filter |
| `position` | query | `string` | no | Optional position abbreviation filter |
