# List Team Recruiting Rankings with College Football Data

Retrieves team recruiting rankings from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/recruiting/teams`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Team Recruiting Rankings](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Optional year filter |
| `team` | query | `string` | no | Optional team filter |
