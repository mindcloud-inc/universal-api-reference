# List Rankings with College Football Data

Retrieves historical poll rankings from College Football Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/rankings`
- **Base URL:** `https://api.collegefootballdata.com`
- **Official documentation:** [List Rankings](https://api.collegefootballdata.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | yes | Required year filter |
| `seasonType` | query | `string` | no | Optional season type filter |
| `week` | query | `number` | no | Optional week filter |
