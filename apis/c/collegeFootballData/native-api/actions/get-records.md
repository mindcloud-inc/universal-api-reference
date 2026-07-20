# List Records with College Football Data

Retrieves historical team records from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/records`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Records](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if team not specified |
| `team` | query | `string` | no | Team filter, required if year not specified |
| `conference` | query | `string` | no | Optional conference filter |
