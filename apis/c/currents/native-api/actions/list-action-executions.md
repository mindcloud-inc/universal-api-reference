# List Action Executions with Currents

## Endpoint

- **Method:** `GET`
- **Path:** `/actions/:actionId/tests`
- **Base URL:** `https://api.currents.dev/v1`
- **Official documentation:** [List Action Executions](https://docs.currents.dev/api/resources)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `actionId` | path | `string` | yes |
| `date_end` | query | `string` | yes |
| `date_start` | query | `string` | yes |
