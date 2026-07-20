# Get Stack Diagnostics with Logit

Retrieves stack diagnostics from Logit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/stacks/:stackId/diagnostics`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [Get Stack Diagnostics](https://logit.io/docs/developer-api/security-and-diagnostics/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stackId` | path | `string` | yes |
| `Component` | query | `string` | no |
| `Level` | query | `string` | no |
| `SearchTerm` | query | `string` | no |
| `TimeRange` | query | `string` | no |
| `Page` | query | `number` | yes |
| `PageSize` | query | `number` | yes |
