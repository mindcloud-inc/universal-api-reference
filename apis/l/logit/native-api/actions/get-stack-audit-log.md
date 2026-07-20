# Get Stack Audit Log with Logit

Retrieves a stack audit log from Logit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/stacks/:stackId/audit-log`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [Get Stack Audit Log](https://logit.io/docs/developer-api/managing-stacks/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stackId` | path | `string` | yes |
| `Search` | query | `string` | no |
| `Page` | query | `number` | yes |
| `PageSize` | query | `number` | yes |
| `Period` | query | `number` | no |
