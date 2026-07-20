# Get Alert Rule with Umbrella

Retrieves an alert rule from Umbrella.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.sse.cisco.com/admin/v2/alerting/rules/:ruleId`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Get Alert Rule](https://developer.cisco.com/docs/cloud-security/get-alert-rule/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `string` | no | The alert rule ID. |
