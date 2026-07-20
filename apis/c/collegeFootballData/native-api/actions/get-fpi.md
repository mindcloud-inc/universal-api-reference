# List F P I with College Football Data

Retrieves historical FPI ratings from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ratings/fpi`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List F P I](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | year filter, required if team not specified |
| `team` | query | `string` | no | team filter, required if year not specified |
| `conference` | query | `string` | no | Optional conference filter |
