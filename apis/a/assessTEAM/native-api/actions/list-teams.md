# List Teams with AssessTEAM

Retrieves the teams report from AssessTEAM.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/teams`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [List Teams](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamname` | query | `string` | no | Team name, for example Testing team. |
| `averageresultareascore` | query | `number` | no | Average result area score, for example 7. |
