# Get Service Orders with PestPac

## Endpoint

- **Method:** `GET`
- **Path:** `ServiceOrders`
- **Base URL:** `https://api.workwave.com/pestpac/v1/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderType` | query | `string` | no | — |
| `branch` | query | `string` | no | — |
| `startWorkDate` | query | `string` | no | Use the format "YYYY-MM-DD" |
| `endWorkDate` | query | `string` | no | Use the format "YYYY-MM-DD" |
| `posted` | query | `boolean` | no | — |
| `orderNum` | query | `string` | no | — |
| `inProgress` | query | `boolean` | no | — |
