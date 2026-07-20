# List Player Usage with College Football Data

Retrieves player usage data from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/player/usage`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Player Usage](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `conference` | query | `string` | no | Optional conference abbreviation filter |
| `position` | query | `string` | no | Optional position abbreivation filter |
| `team` | query | `string` | no | Optional team filter |
| `playerId` | query | `number` | no | Optional player id filter |
| `excludeGarbageTime` | query | `boolean` | no | Optional exclude garbage time flag, defaults to false |
