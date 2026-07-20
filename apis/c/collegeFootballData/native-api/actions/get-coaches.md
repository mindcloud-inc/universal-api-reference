# List Coaches with College Football Data

Retrieves historical head coach records from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/coaches`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Coaches](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | query | `string` | no | Optional first name filter |
| `lastName` | query | `string` | no | Optional last name filter |
| `team` | query | `string` | no | Optional team filter |
| `year` | query | `number` | no | Optional year filter |
| `minYear` | query | `number` | no | Optional start year range filter |
| `maxYear` | query | `number` | no | Optional end year range filter |
