# Get Affected Test Executions with Currents

## Endpoint

- **Method:** `GET`
- **Path:** `/actions/tests/:signature`
- **Base URL:** `https://api.currents.dev/v1`
- **Official documentation:** [Get Affected Test Executions](https://docs.currents.dev/api/resources)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date_end` | query | `string` | yes |
| `date_start` | query | `string` | yes |
| `projectId` | query | `string` | yes |
| `signature` | path | `string` | yes |
