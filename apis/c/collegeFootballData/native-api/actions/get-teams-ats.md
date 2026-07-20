# List Teams A T S with College Football Data

Retrieves team ATS summaries from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/ats`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Teams A T S](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `conference` | query | `string` | no | Optional conference filter |
| `team` | query | `string` | no | Optional team filter |
