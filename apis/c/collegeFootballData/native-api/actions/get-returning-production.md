# List Returning Production with College Football Data

Retrieves returning production data from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/player/returning`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Returning Production](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if team not specified |
| `team` | query | `string` | no | Team filter, required if year not specified |
| `conference` | query | `string` | no | Optional conference filter |
