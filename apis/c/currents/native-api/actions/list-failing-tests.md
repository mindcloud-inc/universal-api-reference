# List Failing Tests with Currents

## Endpoint

- **Method:** `GET`
- **Path:** `/tests/:projectId`
- **Base URL:** `https://api.currents.dev/v1`
- **Official documentation:** [List Failing Tests](https://docs.currents.dev/resources/api/api-resources/tests)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date_end` | query | `string` | yes |
| `date_start` | query | `string` | yes |
| `projectId` | path | `string` | yes |
