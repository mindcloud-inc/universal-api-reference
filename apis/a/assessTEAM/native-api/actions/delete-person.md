# Delete Person with AssessTEAM

Deletes an existing person from AssessTEAM.

## Endpoint

- **Method:** `POST`
- **Path:** `/person/deleteperson`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [Delete Person](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personcode` | query | `string` | yes | Unique person code, for example 1001. |
| `w` | query | `boolean` | no | Delete the person together with associated details when true. |
