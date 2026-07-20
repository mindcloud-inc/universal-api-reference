# Get Stack Alert Rule with Logit

Retrieves a stack alert rule from Logit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/stacks/:stackId/alerting/rules/:ruleId`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [Get Stack Alert Rule](https://logit.io/docs/developer-api/alerting-via-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stackId` | path | `string` | yes |
| `ruleId` | path | `string` | yes |
