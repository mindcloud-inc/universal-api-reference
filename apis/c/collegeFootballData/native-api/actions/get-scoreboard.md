# List Scoreboard with College Football Data

Retrieves live scoreboard data from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/scoreboard`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Scoreboard](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classification` | query | `string` | no | Optional division classification filter, defaults to fbs |
| `conference` | query | `string` | no | Optional conference filter |
