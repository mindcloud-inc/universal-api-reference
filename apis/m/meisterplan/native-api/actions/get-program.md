# Get Program with Meisterplan

Retrieves a program from Meisterplan.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios/:scenarioId/programs/:programId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Get Program](https://api.us.meisterplan.com/docs/api.html#operation/GetProgramById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `programId` | path | `string` | yes | Internal Meisterplan program identifier. |
