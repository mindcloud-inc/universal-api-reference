# Create Program with Meisterplan

Creates a new program in Meisterplan.

## Endpoint

- **Method:** `POST`
- **Path:** `/scenarios/:scenarioId/programs`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Create Program](https://api.us.meisterplan.com/docs/api.html#operation/CreateProgram)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `name` | body | `string` | yes | Program name. |
| `programKey` | body | `string` | no | Unique Meisterplan program key. |
