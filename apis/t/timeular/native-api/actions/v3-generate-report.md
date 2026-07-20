# V3 Generate Report with Timeular

Generates a time entry report in the Timeular v3 API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/report/:start/:end`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Generate Report](https://developers.early.app/#f9bed9f5-6fbe-4062-9881-76b117430eb2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end` | path | `string` | yes |
| `start` | path | `string` | yes |
| `timezone` | query | `string` | no |
