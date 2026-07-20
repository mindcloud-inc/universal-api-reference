# List Predicted Points Added By Team with College Football Data

Retrieves team PPA metrics by season from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ppa/teams`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Predicted Points Added By Team](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if team not specified |
| `team` | query | `string` | no | Team filter, required if year not specified |
| `conference` | query | `string` | no | Conference abbreviation filter |
| `excludeGarbageTime` | query | `boolean` | no | Exclude garbage time plays |
