# Search Players with College Football Data

Finds players in College Football Data by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/player/search`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [Search Players](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchTerm` | query | `string` | yes | Search term for matching player name |
| `year` | query | `number` | no | Optional year filter |
| `team` | query | `string` | no | Optional team filter |
| `position` | query | `string` | no | Optional position abbreviation filter |
