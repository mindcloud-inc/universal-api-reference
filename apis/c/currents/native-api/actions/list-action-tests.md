# List Action Tests with Currents

## Endpoint

- **Method:** `GET`
- **Path:** `/actions/:actionId/tests`
- **Base URL:** `https://api.currents.dev/v1`
- **Official documentation:** [List Action Tests](https://docs.currents.dev/api/resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionId` | path | `string` | yes | — |
| `date_start` | query | `string` | yes | Start date in ISO 8601 format. |
| `date_end` | query | `string` | yes | End date in ISO 8601 format. |
