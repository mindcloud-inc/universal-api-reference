# V2 Generate Report with Timeular

Generates a time entry report in the Timeular v2 API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/report/:start/:end`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V2 Generate Report](https://developers.early.app/#dea2c10c-3376-4f43-a2a1-8f8c35fd46a1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end` | path | `string` | yes |
| `start` | path | `string` | yes |
| `timezone` | query | `string` | no |
