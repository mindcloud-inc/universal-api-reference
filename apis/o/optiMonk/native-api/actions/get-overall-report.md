# Get Overall Report with OptiMonk

Retrieves the overall report from OptiMonk.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/`
- **Base URL:** `https://api.optimonk.com/v1`
- **Official documentation:** [Get Overall Report](https://api.optimonk.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupBy` | query | `string` | no | Report grouping granularity. |
| `from` | query | `string` | no | Start date or datetime. |
| `to` | query | `string` | no | End date or datetime. |
