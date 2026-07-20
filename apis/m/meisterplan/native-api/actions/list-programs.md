# List Programs with Meisterplan

Retrieves a list of programs from Meisterplan.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios/:scenarioId/programs`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [List Programs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllPrograms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `pageSize` | query | `number` | no | Number of results to return. |
| `pageAfter` | query | `string` | no | Cursor after which to retrieve results. |
| `filter` | query | `string` | no | Stringified JSON filter object. |
