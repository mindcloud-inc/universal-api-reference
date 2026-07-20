# List Advanced Season Stats with College Football Data

Retrieves advanced team season statistics from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/stats/season/advanced`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Advanced Season Stats](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Year filter, required if team not specified |
| `team` | query | `string` | no | Team filter, required if year not specified |
| `excludeGarbageTime` | query | `boolean` | no | Garbage time exclusion filter, defaults to false |
| `startWeek` | query | `number` | no | Optional start week range filter |
| `endWeek` | query | `number` | no | Optional end week range filter |
