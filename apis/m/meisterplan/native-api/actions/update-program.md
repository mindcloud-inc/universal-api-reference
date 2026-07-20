# Update Program with Meisterplan

Updates an existing program in Meisterplan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/scenarios/:scenarioId/programs/:programId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Update Program](https://api.us.meisterplan.com/docs/api.html#operation/UpdateProgram)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `programId` | path | `string` | yes | Internal Meisterplan program identifier. |
| `name` | body | `string` | no | Updated program name. |
