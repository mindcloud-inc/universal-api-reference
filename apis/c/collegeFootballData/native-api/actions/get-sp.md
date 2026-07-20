# List S P with College Football Data

Retrieves SP+ ratings from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ratings/sp`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List S P](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if team not specified |
| `team` | query | `string` | no | Team filter, required if year not specified |
