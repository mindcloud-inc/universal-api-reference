# List Roster with College Football Data

Retrieves historical team rosters from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/roster`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Roster](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | query | `string` | no | Optional team filter |
| `year` | query | `number` | no | Optional year filter, defaults to 2025 |
| `classification` | query | `string` | no | Optional filter to only include players from FBS or FCS teams |
