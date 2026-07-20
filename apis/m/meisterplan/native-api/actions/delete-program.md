# Delete Program with Meisterplan

Deletes an existing program from Meisterplan.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/scenarios/:scenarioId/programs/:programId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Delete Program](https://api.us.meisterplan.com/docs/api.html#operation/DeleteProgram)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `programId` | path | `string` | yes | Internal Meisterplan program identifier. |
