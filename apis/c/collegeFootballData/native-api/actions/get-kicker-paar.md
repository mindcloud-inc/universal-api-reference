# List Kicker Paar with College Football Data

Retrieves kicker PAAR ratings from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/wepa/players/kicking`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Kicker Paar](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Optional year filter |
| `team` | query | `string` | no | Optional team filter |
| `conference` | query | `string` | no | Optional conference abbreviation filter |
