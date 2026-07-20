# Delete Stack Alert Rule with Logit

Deletes an existing stack alert rule from Logit.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/stacks/:stackId/alerting/rules/:ruleId`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [Delete Stack Alert Rule](https://logit.io/docs/developer-api/alerting-via-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stackId` | path | `string` | yes |
| `ruleId` | path | `string` | yes |
