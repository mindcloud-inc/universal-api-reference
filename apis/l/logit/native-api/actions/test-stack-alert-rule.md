# Test Stack Alert Rule with Logit

Tests a stack alert rule in Logit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/stacks/:stackId/alerting/rules/:ruleId/test`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [Test Stack Alert Rule](https://logit.io/docs/developer-api/alerting-via-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stackId` | path | `string` | yes |
| `ruleId` | path | `string` | yes |
