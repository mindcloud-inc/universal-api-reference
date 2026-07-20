# List Teams with College Football Data

Retrieves team information from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Teams](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conference` | query | `string` | no | Optional conference abbreviation filter |
| `year` | query | `number` | no | Optional year filter to get historical conference affiliations |
