# Create Alert Rule with Umbrella

Creates a new alert rule in Umbrella.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.sse.cisco.com/admin/v2/alerting/rules`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Create Alert Rule](https://developer.cisco.com/docs/cloud-security/create-alert-rule/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Short description for the alert rule. |
| `name` | body | `string` | yes | The alert rule name. |
| `severity` | body | `number` | yes | 1 High, 2 Medium, 3 Low, 4 Info. |
| `status` | body | `number` | yes | 1 enabled, 2 disabled. |
| `rule_type_id` | body | `number` | yes | The alert rule type ID. |
| `notification_info.0.type` | body | `string` | yes | email or webhook. |
| `notification_info.0.recipients.0` | body | `string` | yes | First email recipient. |
| `conditions.match_type` | body | `string` | yes | all or any. |
| `conditions.rows.0.field` | body | `string` | yes | First condition field. |
| `conditions.rows.0.value` | body | `string` | yes | First condition value. |
| `conditions.rows.1.field` | body | `string` | yes | Second condition field. |
| `conditions.rows.1.value` | body | `string` | yes | Second condition value. |
