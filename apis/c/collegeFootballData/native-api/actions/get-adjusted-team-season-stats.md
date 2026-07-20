# List Adjusted Team Season Stats with College Football Data

Retrieves opponent-adjusted team season statistics from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/wepa/team/season`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Adjusted Team Season Stats](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Optional year filter |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference filter |
