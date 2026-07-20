# List Draft Picks with College Football Data

Retrieves historical NFL draft picks from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/draft/picks`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Draft Picks](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Optional year filter |
| `team` | query | `string` | no | Optional NFL team filter |
| `school` | query | `string` | no | Optional college team filter |
| `conference` | query | `string` | no | Optional college conference filter |
| `position` | query | `string` | no | Optional position classification filter |
