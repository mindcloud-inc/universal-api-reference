# Retrieve Audit Logs with Mode

Retrieve audit log events for a Mode workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/audit_logs`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Retrieve Audit Logs](https://mode.com/developer/api-reference/management/audit-logs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_timestamp` | query | `string` | yes | Start of the audit-log time range in ISO 8601 format. |
| `end_timestamp` | query | `string` | yes | End of the audit-log time range in ISO 8601 format. |
