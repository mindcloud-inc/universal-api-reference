# Run a Report with Quickbase

Runs a Quickbase report and returns its results.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/reports/:reportId/run`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Run a Report](https://developer.quickbase.com/operation/runReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | query | `string` | yes | The Quickbase table identifier. |
| `reportId` | path | `string` | yes | The Quickbase report identifier. |
| `skip` | query | `number` | no | The number of rows to skip before returning report results. |
| `top` | query | `number` | no | The maximum number of rows to return. |
