# Get Person with AssessTEAM

Retrieves a person by person code from AssessTEAM.

## Endpoint

- **Method:** `POST`
- **Path:** `/person/getperson`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [Get Person](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personcode` | query | `string` | yes | Unique person code, for example 1001. |
