# List Recruits with College Football Data

Retrieves player recruiting rankings from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/recruiting/players`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Recruits](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required when no team specified |
| `team` | query | `string` | no | Team filter, required when no team specified |
| `position` | query | `string` | no | Optional position categorization filter |
| `state` | query | `string` | no | Optional state/province filter |
| `classification` | query | `string` | no | Optional recruit type classification filter, defaults to HighSchool |
