# Get Stack Alert Rule Status with Logit

Retrieves stack alert rule status from Logit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/stacks/:stackId/alerting/rules/:ruleId/status`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [Get Stack Alert Rule Status](https://logit.io/docs/developer-api/alerting-via-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stackId` | path | `string` | yes |
| `ruleId` | path | `string` | yes |
