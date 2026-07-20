# Update Alert Rule with Umbrella

Updates an existing alert rule in Umbrella.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://api.sse.cisco.com/admin/v2/alerting/rules/:ruleId`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Update Alert Rule](https://developer.cisco.com/docs/cloud-security/update-alert-rule/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated description. |
| `ruleId` | path | `string` | no | The alert rule ID. |
| `status` | body | `number` | no | 1 enabled, 2 disabled. |
