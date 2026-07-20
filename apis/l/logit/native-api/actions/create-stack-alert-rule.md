# Create Stack Alert Rule with Logit

Creates a new stack alert rule in Logit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/stacks/:stackId/alerting/rules`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [Create Stack Alert Rule](https://logit.io/docs/developer-api/alerting-via-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stackId` | path | `string` | yes |
| `newFileName` | body | `string` | yes |
| `templateFileName` | body | `string` | no |
